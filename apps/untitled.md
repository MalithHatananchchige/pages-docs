# Email

Pages Email app is a web-based email client designed and developed exclusively for Pages framework. It has a responsive design to work flawlessly across many devices. Please note that current version only includes the Inbox and Compose views. This is a work in progress and we're hoping to make this a complete jQuery plugin soon

## **Dependencies**

Include the stylesheets of the libraries

```markup
<link href="assets/plugins/jquery-menuclipper/jquery.menuclipper.css" rel="stylesheet" type="text/css" />
```

Include the scripts

```markup
<script src="assets/plugins/quill/quill.min.js" type="text/javascript"></script>
<script src="assets/plugins/jquery-menuclipper/jquery.menuclipper.js"></script>
```

Pages Email Lib

In `pages.email.js` please replace the URL “http://pages.revox.io/json/emails.json” \(Line \#54\) with your own end point URL which can return a JSON having a structure mentioned below. Then include the updated file below `pages.js`.

```markup
<script src="pages/js/pages.email.js"></script>
```

{% hint style="info" %}
Use the following formate for emails
{% endhint %}

* emails - \(Array\) List of all emails categorized by date
  * group - Date category
  * list - list of emails received for the day
    * id - unique ID to represent each email, should be an unique integer
    * subject - Subject line of the email
    * to - \(Array\) Recipients name list
    * body - Email body. HTML is allowed
    * time - Time email was sent
    * datetime - Date and time combined
    * from - Sender name
    * dp - Display picture of the sender
    * dpRetina - Retina version of the display picture of the sender

## Sample JSON output

```javascript
{
    "emails": [
        {
            "group": "Today April 23",
            "list": [{
                "id": 1,
                "subject": "Pages - Multi-Purpose Admin Template Revolution Begins here!",
                "to": ["David Nester", "Jane Smith"],
                "body": "<p>First email body</p> ",
                "time": "5 Mins ago",
                "datetime": "Today at 1:33pm",
                "from": "David Nester",
                "dp": "assets/img/profiles/avatar.jpg",
                "dpRetina": "assets/img/profiles/avatar2x.jpg"
            }, {
                "id": 2,
                "subject": "Your site has some very imaginative animation /movement! ",
                "to": ["Anne Simons"],
                "body": "<p>Second email body</p> ",
                "time": "45 mins ago",
                "datetime": "Today at 1:33pm",
                "from": "Anne Simons",
                "dp": "assets/img/profiles/5.jpg",
                "dpRetina": "assets/img/profiles/5x.jpg"
            }]
        }, {
            "group": "Yesterday April 22",
            "list": [{
                "id": 3,
                "subject": "Good design is obvious. Great design is transparent",
                "to": ["John Doe", "Anne Simons"],
                "body": "<p>Third email body</p> ",
                "time": "1:33pm",
                "datetime": "Today at 1:33pm",
                "from": "David Nester",
                "dp": "assets/img/profiles/b.jpg",
                "dpRetina": "assets/img/profiles/b2x.jpg"
            }]
        }
    ]
}
```

## **Markup**

Inlcude the following HTML source in your file

### **Inbox view**

```markup
<!-- START EMAIL -->
<div class="email-wrapper">
    <!-- START EMAIL SIDEBAR MENU-->
    <nav class="email-sidebar padding-30">
        <a href="email_compose.html" class="btn btn-complete btn-block btn-compose m-b-30">Compose</a>
        <p class="menu-title">BROWSE</p>
        <ul class="main-menu">
            <li class="active">
                <a href="#">
                    <span class="title"><i class="pg-inbox"></i> Inbox</span>
                    <span class="badge pull-right">5</span>
                </a>
            </li>
            <li class="">
                <a href="#">
                    <span class="title"><i class="pg-folder"></i> All mail</span>
                </a>
                <ul class="sub-menu no-padding">
                    <li>
                        <a href="#">
                            <span class="title">Important</span>
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            <span class="title">Labeled</span>
                        </a>
                    </li>
                </ul>
            </li>
            <li>
                <a href="#">
                    <span class="title"><i class="pg-sent"></i> Sent</span>
                </a>
            </li>
            <li>
                <a href="#">
                    <span class="title"><i class="pg-spam"></i> Spam</span>
                    <span class="badge pull-right">10</span>
                </a>
            </li>
        </ul>
        <p class="menu-title m-t-20 all-caps">Quick view</p>
        <ul class="sub-menu no-padding">
            <li>
                <a href="#">
                    <span class="title">Documents</span>
                </a>
            </li>
            <li>
                <a href="#">
                    <span class="title">Flagged</span>
                    <span class="badge pull-right">5</span>
                </a>
            </li>
            <li>
                <a href="#">
                    <span class="title">Images</span>
                </a>
            </li>
        </ul>
    </nav>
    <!-- END EMAL SIDEBAR MENU -->
    <!-- START EMAILS LIST -->
    <div class="email-list b-r b-grey"> <a class="email-refresh" href="#"><i class="fa fa-refresh"></i></a>
        <div id="emailList">
            <!-- START EMAIL LIST SORTED BY DATE -->
            <!-- END EMAIL LIST SORTED BY DATE -->
        </div>
    </div>
    <!-- END EMAILS LIST -->
    <!-- START OPENED EMAIL -->
    <div class="email-opened">
        <div class="no-email">
            <h1>No email has been selected</h1>
        </div>
        <div class="email-content-wrapper">
            <div class="actions-wrapper menuclipper bg-master-lightest">
                <ul class="actions menuclipper-menu no-margin p-l-20 ">
                    <li class="visible-sm-inline-block visible-xs-inline-block">
                        <a href="#" class="email-list-toggle"><i class="fa fa-angle-left"></i> All Inboxes
                                </a>
                    </li>
                    <li class="no-padding "><a href="#" class="text-info">Reply</a>
                    </li>
                    <li class="no-padding "><a href="#">Reply all</a>
                    </li>
                    <li class="no-padding "><a href="#">Forward</a>
                    </li>
                    <li class="no-padding "><a href="#">Mark as read</a>
                    </li>
                    <li class="no-padding "><a href="#" class="text-danger">Delete</a>
                    </li>
                </ul>
                <div class="clearfix"></div>
            </div>
            <div class="email-content">
                <div class="email-content-header">
                    <div class="thumbnail-wrapper d48 circular bordered">
                        <img width="40" height="40" alt="" data-src-retina="assets/img/profiles/avatar2x.jpg" data-src="assets/img/profiles/avatar.jpg" src="assets/img/profiles/avatar2x.jpg">
                    </div>
                    <div class="sender inline m-l-10">
                        <p class="name no-margin bold">
                        </p>
                        <p class="datetime no-margin"></p>
                    </div>
                    <div class="clearfix"></div>
                    <div class="subject m-t-20 m-b-20 semi-bold">
                    </div>
                    <div class="fromto">
                        <div class="pull-left">
                            <div class="btn-group dropdown-default">
                                <a class="btn dropdown-toggle btn-small btn-rounded" data-toggle="dropdown" href="#">
                                        David Nester
                                        <span class="caret"></span>
                                        </a>
                                <ul class="dropdown-menu">
                                    <li><a href="#">Action</a>
                                    </li>
                                    <li><a href="#">Friend</a>
                                    </li>
                                    <li><a href="#">Report</a>
                                    </li>
                                </ul>
                            </div>
                            <label class="inline">
                                <span class="muted">&nbsp;&nbsp;to</span>
                                <span class=" small-text">johnsmith@skyace.com</span>
                            </label>
                        </div>
                    </div>
                </div>
                <div class="clearfix"></div>
                <div class="email-content-body m-t-20">
                </div>
                <div class="wysiwyg5-wrapper b-a b-grey m-t-30">
                    <textarea class="email-reply" placeholder="Reply"></textarea>
                </div>
            </div>
        </div>
    </div>
    <!-- END OPENED EMAIL -->
    <!-- START COMPOSE BUTTON FOR TABS -->
    <div class="compose-wrapper visible-xs">
        <a class="compose-email text-info pull-right m-r-10 m-t-10" href="email_compose.html"><i class="fa fa-pencil-square-o"></i></a>
    </div>
    <!-- END COMPOSE BUTTON -->
</div>
<!-- END EMAIL -->
```

### **Compose view**

Replace `<div class="email-opened">...</div>` with the following for the compose view

```markup
<!-- START COMPOSE EMAIL -->
<div class="email-composer container-fluid">
    <div class="row">
        <div class="col-sm-12 no-padding">
            <div class="wysiwyg5-wrapper email-toolbar-wrapper">
            </div>
            <form id="form-project" role="form" autocomplete="off">
                <div class="form-group-attached">
                    <div class="row clearfix">
                        <div class="col-sm-6">
                            <div class="form-group form-group-default">
                                <label>TO:</label>
                                <input name="to" data-role="tagsinput" class="form-control tagsinput" type="text" value="John Smith" />
                            </div>
                        </div>
                        <div class="col-sm-6">
                            <div class="form-group form-group-default">
                                <label>CC:</label>
                                <input type="text" class="form-control" name="cc" placeholder="Add Carbon Copy">
                            </div>
                        </div>
                    </div>
                    <div class="form-group form-group-default">
                        <label>Subject</label>
                        <input type="text" class="form-control" name="subject">
                    </div>
                </div>
            </form>
            <div class="wysiwyg5-wrapper email-body-wrapper">
                <textarea class="wysiwyg email-body" style="height:350px"></textarea>
            </div>
        </div>
    </div>
    <div class="row p-b-20">
        <div class="col-sm-11">
            <button class="btn btn-white btn-cons">Cancel</button>
            <button class="btn btn-complete btn-cons m-l-10">Send</button>
            <div class="checkbox inline m-l-20">
                <input type="checkbox" value="1" id="sendCC">
                <label for="sendCC" class="hint-text hidden-xs">Send a <span class="text-complete">Carbon Copy</span> CC to my Primary email address.</label>
                <label for="sendCC" class="hint-text visible-xs-inline">Send me a CC</label>
            </div>
        </div>
        <div class="col-sm-1">
            <button class="btn btn-complete pull-right">
                <i class="pg-save"></i>
            </button>
        </div>
    </div>
</div>
<!-- END COMPOSE EMAIL -->
```

