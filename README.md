Invoice Generator
Description
This project is a simple, client-side invoice generator implemented in HTML, CSS, and JavaScript. It creates a professional-looking invoice based on input data, without requiring any server-side processing.
Features

Generates a detailed invoice with seller, billing, and shipping information
Calculates total amounts including taxes
Supports multiple line items
Converts total amount to words
Responsive design for various screen sizes

How to Use

Clone or download this repository to your local machine.
Open the index.html file in a web browser.
The invoice will be generated automatically using the sample data provided in the invoiceData object.

Customizing the Invoice
To generate an invoice with your own data:

Open the index.html file in a text editor.
Locate the invoiceData object in the <script> section at the bottom of the file.
Modify the invoiceData object with your own information. Here's an example of the structure:

javascriptCopyconst invoiceData = {
    sellerDetails: {
        name: 'Your Company Name',
        address: 'Your Address',
        city: 'Your City',
        state: 'Your State',
        pincode: 'Your Pincode',
        panNo: 'Your PAN',
        gstRegistrationNo: 'Your GST No'
    },
    billingDetails: {
        // ... (similar structure to sellerDetails)
    },
    shippingDetails: {
        // ... (similar structure to sellerDetails)
    },
    placeOfSupply: 'Place of Supply',
    placeOfDelivery: 'Place of Delivery',
    orderDetails: {
        orderNo: 'Order Number',
        orderDate: 'Order Date'
    },
    invoiceDetails: {
        invoiceNo: 'Invoice Number',
        invoiceDetails: 'Invoice Details',
        invoiceDate: 'Invoice Date'
    },
    reverseCharge: false,
    items: [
        {
            description: "Item Description",
            unitPrice: 100.00,
            quantity: 1,
            discount: 0
        },
        // Add more items as needed
    ]
};

Save the file and refresh the page in your web browser to see the updated invoice.

Customizing the Design
The invoice design can be customized by modifying the CSS in the <style> section of the HTML file. You can change colors, fonts, sizes, and layout to match your brand or preferences.
Features

Automatic Calculations: The script automatically calculates net amounts, tax amounts, and total amounts based on the provided item data.
Tax Handling: The system determines whether to apply CGST & SGST or IGST based on the place of supply and delivery.
Input Validation: The script includes basic validation to ensure all required data is present and correctly formatted.
Responsive Design: The invoice layout is designed to be responsive and should display well on various screen sizes.

Limitations

This is a client-side only solution and does not include any backend for storing or retrieving invoice data.
The current implementation does not include printing functionality, though the page can be printed using the browser's print function.
The invoice number and other details are static and would need to be manually updated for each new invoice.

Future Improvements

Add a form interface for easy data input
Implement a backend system for storing and retrieving invoice data
Add functionality to save invoices as PDF
Implement a proper printing solution
Add support for multiple currencies

Contributing
Feel free to fork this project and submit pull requests with any enhancements you develop. For major changes, please open an issue first to discuss what you would like to change.
License
This project is open source and available under the MIT License.
