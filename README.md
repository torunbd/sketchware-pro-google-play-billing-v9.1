# Sketchware Pro Google Play Billing v9.1

A ready-to-use Sketchware Pro project demonstrating **Google Play Billing Library 9.1.0**.

This project is designed to help Sketchware Pro developers easily integrate Google Play in-app purchases and subscriptions into their Android applications.

## Ready to Use – No Extra Setup Required

**The included SWB file is ready to use!**

All required project configurations, setup, and included libraries are already provided inside the project. You do not need to download or install libraries separately.

### How to Use

1. Download the `.swb` file from the `SWB/` folder.
2. Import it into Sketchware Pro.
3. Open the project.
4. Customize the UI, product IDs, subscription plans, and features according to your app's requirements.
5. Configure matching products and base plans in your Google Play Console.
6. Test your app before publishing.

**Import, customize, and use!**

The project is provided as a ready-to-use starting point. You can adapt it to your own application and requirements.

> **Important:** Google Play Console configuration is still required for real purchases. Your product IDs and subscription base plan IDs in Google Play Console must match those used in the project.

## Features

- Google Play Billing Library 9.1.0
- Ready-to-import Sketchware Pro SWB project
- Complete source project ZIP
- Subscription support
- Multiple subscription base plans
- Lifetime one-time purchase support
- Dynamic product pricing from Google Play
- Subscription offer token handling
- Purchase flow and acknowledgement
- Restore purchases
- Subscription management
- Billing connection and retry handling
- Duplicate purchase-flow prevention
- Local Pro status management

## Project Downloads

| File | Description |
|---|---|
| `SWB/GooglePlayBilling_v9.1.swb` | Ready-to-use Sketchware Pro project |
| `Source-Code/GooglePlayBilling_v9.1_Source.zip` | Complete source project ZIP |

## Requirements

- Sketchware Pro
- Android device for testing
- Google Play Console developer account for real purchase testing
- An application configured with Google Play Billing

**No separate library download is required for the included SWB project.**

## Google Play Console Configuration

The included project uses these product IDs:

### 1. Subscription Product

Create one subscription product:

- Product ID: `pro_sub`

Add the following four base plans:

| Plan | Base Plan ID | Billing Period |
|---|---|---|
| 1 Month | `pro-1month` | 1 Month |
| 3 Months | `pros-3month` | 3 Months |
| 6 Months | `pro-6month` | 6 Months |
| 1 Year | `pro-1year` | 1 Year |

**Important:** Use the exact base plan IDs shown above, including spelling, so they match the project code.

Activate the subscription and configure prices for your target countries.

### 2. Lifetime Product

Create a one-time in-app product:

- Product ID: `pro_lifetime`
- Product type: One-time product
- Purchase type: Non-consumable

Set the price and activate the product.

## Customization

You can customize the project according to your application:

- Change the app interface and design.
- Change product IDs if needed.
- Add or remove subscription plans.
- Set your own prices in Google Play Console.
- Customize Pro status and premium features.
- Integrate the billing functionality into your own app.

If you change product IDs or base plan IDs in the code, make sure the corresponding IDs in Google Play Console match exactly.

## Import Instructions

1. Download `GooglePlayBilling_v9.1.swb`.
2. Open Sketchware Pro.
3. Import the SWB project.
4. Open the imported project.
5. Customize it and configure your Google Play products.

The complete source project is also available in the `Source-Code/` folder.

## Gradle Dependency

The project uses:

```gradle
implementation "com.android.billingclient:billing:9.1.0"
```

The SWB project already includes its required setup and libraries. You do not need to download this dependency separately when importing the included project.

## Testing

Before publishing your application:

1. Upload your app to an Internal Testing track.
2. Add your tester account to the License Testing list.
3. Install the app through Google Play.
4. Test subscription purchases.
5. Test lifetime purchases.
6. Test purchase restoration.
7. Test subscription cancellation and expiration.

## Security Notice

This project demonstrates Google Play Billing integration.

For production applications, purchase verification should be performed securely using a trusted backend and the Google Play Developer API.

Do not rely only on a local SharedPreferences value to determine whether a purchase is valid. Handle expiration, refunds, and revoked purchases properly.

## Troubleshooting

- Make sure your product IDs match Google Play Console.
- Make sure subscription base plan IDs match exactly.
- Ensure your products and base plans are activated.
- Install the app through a Google Play testing track.
- Use a valid License Tester account.
- Check your internet connection and Play Store availability.

## Credits

Developed and shared by **TorunHero Studio**.

Credit or attribution is appreciated but not mandatory. You are welcome to customize this project for your own applications.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

Third-party libraries and dependencies remain subject to their respective licenses.

## Contributing

Suggestions, improvements, and bug reports are welcome. Feel free to contribute and help improve this project.

---

**Developer:** TorunHero Studio  
**GitHub:** https://github.com/torunbd
