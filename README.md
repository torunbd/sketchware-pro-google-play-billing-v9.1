
Sketchware Pro Google Play Billing v9.1

A Ready-to-Use Google Play Billing Project for Sketchware Pro

Developed by TorunHero Studio

""Billing Library" (https://img.shields.io/badge/Google%20Play%20Billing-9.1.0-brightgreen)" (https://developer.android.com/google/play/billing)
""Platform" (https://img.shields.io/badge/Platform-Android-green)" (https://developer.android.com/)
""IDE" (https://img.shields.io/badge/IDE-Sketchware%20Pro-blue)" (https://github.com/Sketchware-Pro/Sketchware-Pro)

About This Project

This repository provides a complete, ready-to-use Sketchware Pro project demonstrating Google Play Billing Library 9.1.0 integration.

It is designed to help Android developers integrate subscription and one-time purchase functionality into their applications without building the entire billing implementation from scratch.

The project includes an importable SWB file and a complete source project in ZIP format.

Features

- Google Play Billing Library 9.1.0
- Ready-to-import Sketchware Pro project
- Complete source project in ZIP format
- Subscription product integration
- Multiple subscription base plans
- Lifetime one-time purchase
- Dynamic product price loading from Google Play
- Subscription offer token handling
- Purchase flow management
- Purchase acknowledgement
- Restore existing purchases
- Billing connection and reconnection handling
- Retry mechanism for temporary connection failures
- Duplicate purchase-flow protection
- Basic local Pro status management
- Subscription management page link
- Purchase status and error messages

Project Downloads

File| Description
"SWB/GooglePlayBilling_v9.1.swb"| Ready-to-import Sketchware Pro project
"Source-Code/GooglePlayBilling_v9.1_Source.zip"| Complete source project

Download or clone this repository to get the project files.

Requirements

- Sketchware Pro
- Android application project
- Google Play Console developer account
- Google Play Billing Library 9.1.0
- Configured subscription and in-app products
- Google Play Store for purchase testing

Google Play Billing Configuration

The example project uses the following product structure.

1. Subscription Product

Product ID:

"pro_sub"

This single subscription product contains four base plans.

Plan| Base Plan ID in the example code| Billing Period
1 Month| "pro-1months"| 1 Month
3 Months| "pros-3months"| 3 Months
6 Months| "pro-6months"| 6 Months
1 Year| "pro-1years"| 1 Year

Important: These IDs must match the constants in the included source code exactly. You can use different IDs, but you must update the corresponding constants in "MainActivity" as well.

2. Lifetime Product

Product ID:

"pro_lifetime"

This is a separate one-time, non-consumable purchase product.

It is intended for users who want permanent access to the Pro features through a single purchase.

How to Import the SWB Project

1. Download "GooglePlayBilling_v9.1.swb" from the "SWB" folder.
2. Open Sketchware Pro.
3. Use the project's SWB import option.
4. Import the downloaded file.
5. Open the imported project.
6. Review the application package name, product IDs and Billing configuration.
7. Build and test the application.

How to Use the Source Code

1. Download "GooglePlayBilling_v9.1_Source.zip".
2. Extract the ZIP file.
3. Import or open the source project using the appropriate Sketchware Pro workflow.
4. Review the billing implementation and project configuration.
5. Change the example package name and product IDs if necessary.
6. Configure your own products in Google Play Console.
7. Build and test your application.

Billing Library Dependency

The example uses Google Play Billing Library version 9.1.0.

For Gradle-based Android projects, the dependency is:

implementation "com.android.billingclient:billing:9.1.0"

Make sure the dependency and project configuration are compatible with your Android build environment.

Testing Purchases

Before releasing your application:

1. Configure the application in Google Play Console.
2. Create and activate the required products and base plans.
3. Upload an application build to an appropriate testing track.
4. Add eligible license testers.
5. Install the application through Google Play using a tester account.
6. Test each subscription plan.
7. Test the lifetime purchase.
8. Test purchase restoration and subscription management.
9. Check pending purchases, cancellation and error handling.

Purchases made by sideloading an APK may not behave like purchases made through Google Play testing tracks.

Important Security Notes

This project demonstrates billing integration and local Pro status handling.

Local SharedPreferences are not secure purchase verification.

The example stores Pro status locally. This is useful for demonstrating application logic, but a modified device or application could manipulate local preferences.

For production applications:

- Verify purchase tokens using a trusted backend and the Google Play Developer API.
- Do not activate premium access based only on a locally stored Boolean value.
- Handle subscription expiration, cancellation, refund and revocation.
- Never expose private API keys, service account credentials or signing keys.
- Follow the current Google Play Billing policies.

Troubleshooting

Billing connection failed

Check the internet connection, Google Play Store availability and Billing configuration.

Product not found

Verify that the product ID is identical in the source code and Google Play Console.

Also make sure the product and its base plans are active and available.

Billing error 5 (DEVELOPER_ERROR)

Check:

- Application package name
- Google Play Console application configuration
- Signing certificate
- Billing dependency
- Product and base plan configuration
- Google Play testing installation

Subscription price not loading

Make sure the subscription product contains active base plans and that the corresponding base plan IDs match the source code.

Purchase already owned

Use the restore purchase functionality and check the user's existing Google Play purchases.

Credit

This project is developed and published by TorunHero Studio.

If you use this project, mentioning TorunHero Studio in your application's About page, credits section or another appropriate location is appreciated.

Attribution to TorunHero Studio is optional. However, the copyright and MIT License notice must be retained as required by the license.

License

This project is distributed under the MIT License.

See the "LICENSE" file for details.

Developer

TorunHero Studio

GitHub: https://github.com/torunbd

Repository: https://github.com/torunbd/sketchware-pro-google-play-billing-v9.1

Contributions

Suggestions, bug reports and improvements are welcome.

You can open a GitHub Issue or submit a Pull Request.

If this project helps you, consider giving the repository a ⭐ Star.

Made for the Sketchware Pro developer community.
