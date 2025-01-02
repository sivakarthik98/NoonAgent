<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Embedded Chatbot</title>

    <!-- Optional: You can add some custom styling -->
    <style>
        .chatbot-container {
            width: 100%;
            height: 600px; /* Adjust the height to fit your layout */
            border: 1px solid #ddd; /* Optional: Add a border to the container */
        }
    </style>
</head>
<body>

    <!-- Chatbot container where the chatbot will be loaded -->
    <div class="chatbot-container">
        <!-- Embedded chatbot script -->
        <script type='text/javascript'>
            function initEmbeddedMessaging() {
                try {
                    // Set the language and initialize the embedded messaging service
                    embeddedservice_bootstrap.settings.language = 'en_US'; // Set language to English (US)
                    
                    // Initialize the embedded service with the provided parameters
                    embeddedservice_bootstrap.init(
                        '00DWU00000CtcCF',  // Your Salesforce Organization ID
                        'Noon_Agent',  // The name of the chat service
                        'https://ustglobalinc3-dev-ed.develop.my.site.com/ESWNoonAgent1735816529386',  // The URL of your service
                        {
                            scrt2URL: 'https://ustglobalinc3-dev-ed.develop.my.salesforce-scrt.com'  // Optional secure URL
                        }
                    );
                } catch (err) {
                    console.error('Error loading Embedded Messaging: ', err);
                }
            };
        </script>

        <!-- Include the bot's bootstrap JavaScript to load and initialize it -->
        <script type='text/javascript' src='https://ustglobalinc3-dev-ed.develop.my.site.com/ESWNoonAgent1735816529386/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>
    </div>

</body>
</html>
