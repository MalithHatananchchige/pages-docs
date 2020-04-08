# Modals

Modals are created using Bootstrap Native Modals, they will work as the same way how it works in bootstrap, but it is styled to pages color scheme. To add a modal to pages please refer following guidelines

{% embed url="https://getbootstrap.com/docs/4.1/components/modal/" caption="Bootstrap Documentation" %}

## **Modal Types**

We have added new options to bootstrap modals and made even awesome, by simply changing a class name you can get the following. There 3 different modals to choose from with 3 different size options for each, varying upt 9 modals  


### **Slide Up**

Simply add the class `slide-up` to main `modal` DIV & wrap `modal-content` with `modal-content-wrapper`, Your HTML tag structure should look like this. You can change the `id` attribute of the modal to anything you want.

```markup
<!-- Modal -->
<div class="modal fade slide-up disable-scroll" id="modalSlideUp" tabindex="-1" role="dialog" aria-labelledby="modalSlideUpLabel" aria-hidden="false">
    <div class="modal-dialog ">
        <div class="modal-content-wrapper">
        <div class="modal-content">
            <div class="modal-header clearfix text-left">
                <button type="button" class="close" data-dismiss="modal" aria-hidden="true">
                  <i class="pg-close fs-14"></i>
                </button>
                <h5>Heading <span class="semi-bold">here</span></h5>
            </div>
            <div class="modal-body">
                Add Your Content here
            </div>
        </div>
        </div>
        <!-- /.modal-content -->
    </div>
</div>
<!-- /.modal-dialog -->
```

### **Stick Up**

Simply add the class `stick-up` to main `modal` DIV. You can change the `id` attribute of the modal to anything you want.

```markup
<!-- MODAL STICK UP  -->
<div class="modal fade stick-up" id="myModal" tabindex="-1" role="dialog" aria-labelledby="myModalLabel" aria-hidden="true">
    <div class="modal-dialog">
        <div class="modal-content">
            <div class="modal-header clearfix text-left">
                <button type="button" class="close" data-dismiss="modal" aria-hidden="true">
                <i class="pg-close fs-14"></i>
                </button>
                <h5>Payment <span class="semi-bold">Information</span></h5>
                <p>We need payment information inorder to process your order</p>
            </div>
            <div class="modal-body">
                <form class="form-default" role="form">
                    <div class="row">
                        <div class="col-sm-12">
                            <div class="form-group">
                                <label>Company Name</label>
                                <input type="email" class="form-control" >
                            </div>
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-sm-8">
                            <div class="form-group">
                                <label>Card Number</label>
                                <input type="text" class="form-control" >
                            </div>
                        </div>
                        <div class="col-sm-4">
                            <div class="form-group">
                                <label>Card Holder</label>
                                <input type="text" class="form-control" >
                            </div>
                        </div>
                    </div>
                </form>
                <div class="row">
                    <div class="col-sm-9">
                        <div class="b-a b-grey b-rad-sm clearfix p-l-10 p-r-10">
                            <div class="pull-left">
                                <h5 class="semi-bold">TOTAL</h5>
                            </div>
                            <div class="pull-right">
                                <h5 class="light">$20.00</h5>
                            </div>
                        </div>
                    </div>
                    <div class="col-sm-3">
                        <button type="button" class="btn btn-primary btn-lg btn-large btn-block" data-dismiss="modal">
                        PAY
                        </button>
                    </div>
                </div>
            </div>
        </div>
        <!-- /.modal-content -->
    </div>
    <!-- /.modal-dialog -->
</div>
<!-- END MODAL STICK UP  -->
```

### **Slide Right**

Simply add the class `slide-right` to main `modal` DIV & wrap `modal-content` with `modal-content-wrapper`, Your HTML tag structure should look like this. You can change the `id` attribute of the modal to anything you want.

```markup
<div class="modal fade slide-right" id="modalSlideLeft" tabindex="-1" role="dialog" aria-labelledby="myModalLabel" aria-hidden="true">
<div class="modal-dialog modal-sm">
    <div class="modal-content-wrapper">
        <div class="modal-content table-block">
            <button type="button" class="close" data-dismiss="modal" aria-hidden="true"><i class="pg-close fs-14"></i></button>
            <div class="modal-body v-align-middle text-center   ">
                <h5 class="text-primary ">Before you <span class="semi-bold">proceed</span>, you have to login to make the necessary changes</h5>
                <br>
                <button type="button" class="btn btn-primary btn-block" data-dismiss="modal">Continue</button>
                <button type="button" class="btn btn-default btn-block" data-dismiss="modal">Cancel</button>
            </div>
        </div>
    </div>
    <!-- /.modal-content -->
</div>
<!-- /.modal-dialog -->
</div>
```

### **Fill In**

Simply add the class `fill-in` to main `modal` DIV. You can change the `id` attribute of the modal to anything you want.

```markup
<div class="modal fade fill-in" id="modalFillIn" tabindex="-1" role="dialog" aria-labelledby="modalFillInLabel" aria-hidden="true">
<button type="button" class="close" data-dismiss="modal" aria-hidden="true">
    <i class="pg-close"></i>
</button>
<div class="modal-dialog ">
    <div class="modal-content">
        <div class="modal-header">
            <h5 class="text-left p-b-5"><span class="semi-bold">News letter</span> signup</h5>
        </div>
        <div class="modal-body">
            <div class="row">
                <div class="col-md-9">
                    <input type="text" placeholder="Your email address here" class="form-control input-lg" id="icon-filter" name="icon-filter">
                </div>
                <div class="col-md-3 text-center">
                    <button type="button" class="btn btn-primary btn-lg btn-large fs-15">Sign up</button>
                </div>
            </div>
            <p class="text-right hinted-text p-t-10 p-r-10">What is it ? Terms and conditions</p>
        </div>
        <div class="modal-footer">

        </div>
    </div>
    <!-- /.modal-content -->
</div>
<!-- /.modal-dialog -->
</div>
```

## **How to Open Bootstrap Modal**

One method is to create a Link or Button with the following attributes `data-toggle="modal" data-target="#myModal"` \*Make sure the data-target value to be the ID of your Modal

eg :

```markup
<!-- Button trigger modal -->
<button class="btn btn-primary btn-lg" data-toggle="modal" data-target="#myModal">
  Launch demo modal
</button>
```

