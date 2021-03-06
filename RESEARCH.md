# Research

Research notes for the implementation of this extension.

## E-mail templates

### Contact Form


### DONE: Credit Memo Update

* Used in model sales/order_creditmemo in method sendUpdateEmail($notifyCustomer = true, $comment = '')
* Variables:
    * 'order'        => $order
    * 'creditmemo'   => $creditmemo
    * 'comment'      => $comment
    * 'billing'      => $order->getBillingAddress()
* Special:
    * In method, customer email address is retrieved from order: $order->getCustomerEmail()


### DONE: Credit Memo Update for Guest

* Same as Credit Memo Update, method selects template depending on $order->getCustomerIsGuest()

### Currency Update Warnings


### Forgot Admin Password


### DONE: Forgot Password
* Template file: account_password_reset_confirmation.html
* Template type: html
* Method: Mage_Customer_Model_Customer::sendPasswordResetConfirmationEmail()
* Template params:
  - customer (Mage_Customer_Model_Customer)
Shouldn't be a problem, just provide the customer object.  

### DONE: Invoice Update

* Used in model sales/order_invoice in method sendUpdateEmail($notifyCustomer = true, $comment = '')
* Variables:
    * 'order'        => $order
    * 'invoice'      => $invoice
    * 'comment'      => $comment
    * 'billing'      => $order->getBillingAddress()
* Special:
    * In method, customer email address is retrieved from order: $order->getCustomerEmail()

### DONE: Invoice Update for Guest

* Same as Invoice update, the method checks whether customer is guest by $order->getCustomerIsGuest()

### Log cleanup Warnings


### Moneybookers activate email


### DONE: New Credit Memo

* Used in model sales/order_creditmemo in method sendEmail($notifyCustomer = true, $comment = '')
* Variables:
    * 'order'        => $order
    * 'creditmemo'   => $creditmemo
    * 'comment'      => $comment
    * 'billing'      => $order->getBillingAddress()
    * 'payment_html' => $paymentBlockHtml
* Special:
    * The payment block is generated in the method using the store emulation
    * In method, customer email address is retrieved from order: $order->getCustomerEmail()

### DONE: New Credit Memo for Guest

* Same as New Credit Memo, the method checks whether customer is guest by $order->getCustomerIsGuest()

### DONE: New Invoice

* Used in model sales/order_invoice in method sendEmail($notifyCustomer = true, $comment = '')
* Variables:
    * 'order'        => $order
    * 'invoice'      => $invoice
    * 'comment'      => $comment
    * 'billing'      => $order->getBillingAddress()
    * 'payment_html' => $paymentBlockHtml
* Special:
    * The payment block is generated in the method using the store emulation
    * In method, customer email address is retrieved from order: $order->getCustomerEmail()

### DONE: New Invoice for Guest

* Same as New Invoice, the method checks whether customer is guest by $order->getCustomerIsGuest()

### DONE: New Order

* Used in model sales/order in method sendNewOrderEmail()
* Variables:
    * 'order'        => $order,
    * 'billing'      => $order->getBillingAddress(),
    * 'payment_html' => $paymentBlockHtml
* Special:
    * The payment block is generated in the method using the store emulation
    * In method, customer email address is retrieved from order: $order->getCustomerEmail()


### DONE: New Order for Guest

* Same as New Order, the method checks whether customer is guest by $order->getCustomerIsGuest()

### DONE: New Shipment

* Used in model sales/order_shipment in method sendEmail($notifyCustomer = true, $comment = '')
* Variables:
    * 'order'        => $order
    * 'shipment'     => $shipment
    * 'comment'      => $comment
    * 'billing'      => $order->getBillingAddress()
    * 'payment_html' => $paymentBlockHtml
* Special:
    * The payment block is generated in the method using the store emulation
    * In method, customer email address is retrieved from order: $order->getCustomerEmail()

### DONE: New Shipment for Guest

* Same as New Shipment, the method checks whether customer is guest by $order->getCustomerIsGuest()

### DONE: New account
* Template file: account_new.html
* Template type: html
* Method: Mage_Customer_Model_Customer::sendNewAccountEmail()
* Template params:
  - customer (Mage_Customer_Model_Customer)
  - backUrl (String, default '')
Shouldn't be a problem, just provide the customer object.  

### DONE: New account confirmation key
* Template file: account_new_confirmation.html
* Template type: html
* Method: Mage_Customer_Model_Customer::sendNewAccountEmail()
* Template params:
  - customer (Mage_Customer_Model_Customer)
  - backUrl (String, default '')
Shouldn't be a problem, just provide the customer object.  

### DONE: New account confirmed
* Template file: account_new_confirmed.html
* Template type: html
* Method: Mage_Customer_Model_Customer::sendNewAccountEmail()
* Template params:
  - customer (Mage_Customer_Model_Customer)
  - backUrl (String, default '')
Shouldn't be a problem, just provide the customer object.  

### DONE:Newsletter subscription confirmation
* Template file: newsletter_subscr_confirm.html
* Template type: html
* Method: Mage_Newsletter_Model_Subscriber::sendConfirmationRequestEmail()
* Template params:
  - subscriber (Mage_Newsletter_Model_Subscriber)
* Notes:
  - inline translation disabled while sending mail
  - does getProcessedTemplate() get called at all?

### DONE:Newsletter subscription success
* Template file: newsletter_subscr_success.html
* Template type: html
* Method: Mage_Newsletter_Model_Subscriber::sendConfirmationSuccessEmail()
* Template params:
  - subscriber (Mage_Newsletter_Model_Subscriber)
* Notes:
  - inline translation disabled while sending mail
  - does getProcessedTemplate() get called at all?  

### DONE:Newsletter unsubscription success
* Template file: newsletter_unsub_success.html
* Template type: html
* Method: Mage_Newsletter_Model_Subscriber::sendUnsubscriptionEmail()
* Template params:
  - subscriber (Mage_Newsletter_Model_Subscriber)
* Notes:
  - inline translation disabled while sending mail
  - does getProcessedTemplate() get called at all?

### DONE: Order Update

* Used in model sales/order in method sendOrderUpdateEmail($notifyCustomer = true, $comment = '')
* Variables:
    * 'order'        => $order
    * 'billing'      => $order->getBillingAddress()
    * 'payment_html' => $paymentBlockHtml
* Special:
    * In method, customer email address is retrieved from order: $order->getCustomerEmail()

### DONE: Order Update for Guest

* Same as Order Update, the method checks whether customer is guest by $order->getCustomerIsGuest()


### Payment Failed


### Product alerts Cron error


### DONE: Product price alert
* Template file: product_price_alert.html
* Template type: html
* Method: Mage_ProductAlert_Model_Email::send()
* Template params:
  * 'customerName'  => $this->_customer->getName(),
  * 'alertGrid'     => $block

### DONE: Product stock alert
* Template file: product_stock_alert.html
* Template type: html
* Method: Mage_ProductAlert_Model_Email::send()
* Template params:
  * 'customerName'  => $this->_customer->getName(),
  * 'alertGrid'     => $block


### DONE: Remind Password
* Template file: password_new.html
* Template type: html
* Method: Mage_Customer_Model_Customer::sendPasswordReminderEmail()
* Template params:
  * customer (Mage_Customer_Model_Customer)
Shouldn't be a problem, just provide the customer object. 

### DONE: Send product to a friend

* Used in model sendfriend/sendfriend in method send()
* Variables:
    * 'name'          => $name
    * 'email'         => $email
    * 'product_name'  => $this->getProduct()->getName()
    * 'product_url'   => $this->getProduct()->getUrlInStore()
    * 'message'       => $message
    * 'sender_name'   => $sender['name']
    * 'sender_email'  => $sender['email']
    * 'product_image' => Mage::helper('catalog/image')->init($this->getProduct(), 'small_image')->resize(75)


### DONE: Share Wishlist
* Template file: wishlist_share.html
* Template type: html
* Method: Mage_Wishlist_controllers_IndexController::sendAction()
* Template params:
  - 'customer'       => $customer,
  - 'salable'        => $wishlist->isSalable() ? 'yes' : '',
  - 'items'          => $wishlistBlock,
  - 'addAllLink'     => Mage::getUrl('*/shared/allcart', array('code' => $sharingCode)),
  - 'viewOnSiteLink' => Mage::getUrl('*/shared/index', array('code' => $sharingCode)),
  - 'message'        => $message

### DONE: Shipment Update

* Used in model sales/order_shipment in method sendUpdateEmail($notifyCustomer = true, $comment = '')
* Variables:
    * 'order'    => $order
    * 'shipment' => $shipment
    * 'comment'  => $comment
    * 'billing'  => $order->getBillingAddress()
* Special:
    * In method, customer email address is retrieved from order: $order->getCustomerEmail()

### DONE: Shipment Update for Guest

* Same as Shipment Update, the method checks whether customer is guest by $order->getCustomerIsGuest()

### DONE: Sitemap generate Warnings
* Template file: sitemap_generate_warning.html
* Template type: text
* Method: Mage_Sitemap_Model_Observer::scheduledGenerateSitemaps()
* Template params:
  - 'warnings' => join("\n", $errors)

### DONE: Token Status Change
* Template file: token.html
* Template type: html
* Method: Mage_Oauth_Helper_Data::sendNotificationOnTokenStatusChange()
* Template params:
    * 'name'            => $userName        // @var string
    * 'userName'        => $userName        // @var string
    * 'email'           => $userEmail       // @var string
    * 'applicationName' => $applicationName // @var string
    * 'status'          => $status          // @var string

## Necessary parameters

* customerId
  - test_product_price_alert_email_template
  - test_product_stock_alert_email_template
  - test_new_account_email_template
  - test_new_account_confirmation_key_email_template
  - test_new_account_confirmed_email_template
  - test_forgot_password_email_template
  - test_remind_password_email_template
  - test_share_wishlist_email_template
* incrementId (Order)
  - test_sales_order_creditmemo_email_template
  - test_sales_order_creditmemo_update_email_template
  - test_sales_order_invoice_email_template
  - test_sales_order_invoice_update_email_template
  - test_sales_order_email_template
  - test_sales_order_update_email_template
  - test_sales_order_shipment_email_template
  - test_sales_order_shipment_update_email_template
* comment (optional)
  - test_sales_order_creditmemo_email_template
  - test_sales_order_creditmemo_update_email_template
  - test_sales_order_invoice_email_template
  - test_sales_order_invoice_update_email_template
  - test_sales_order_email_template
  - test_sales_order_update_email_template
  - test_sales_order_shipment_email_template
  - test_sales_order_shipment_update_email_template
* fromName
  - test_sendfriend_email_template
* fromEmail
  - test_sendfriend_email_template
* toName
  - test_sendfriend_email_template
* toEmail
  - test_sendfriend_email_template
* message
  - test_sendfriend_email_template
* productSku
  - test_sendfriend_email_template
* wishlistId
  - test_share_wishlist_email_template
* (kein Parameter)
  - test_newsleter_subscribe_email_template
  - test_newsletter_subscribe_success_email_template
  - test_newsletter_unsubscribe_success_email_templates
  - test_sitemap_generate_warnings_email_template
  - test_token_status_change_email_template
