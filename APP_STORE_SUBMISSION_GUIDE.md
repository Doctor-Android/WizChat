# WizNet App Store Submission Guide

## iOS App Store Submission

### Prerequisites
1. **Apple Developer Account** ($99/year)
   - Enroll at [developer.apple.com](https://developer.apple.com)
   - Complete identity verification
   - Accept agreements

2. **Xcode** (Latest version)
   - Download from Mac App Store
   - Install iOS development tools

3. **App Store Connect Access**
   - Request access from Apple Developer account
   - Complete tax and banking information

### Step 1: Prepare Your App
```bash
# Navigate to project directory
cd /home/kira/Documents/Ghostz/WizNet

# Run build script
./build-ios.sh

# Open in Xcode
open WizNet.xcodeproj
```

### Step 2: Configure Xcode Project
1. **Bundle Identifier**
   - Set to: `com.wiznet.app`
   - Must be unique across App Store

2. **Version & Build**
   - Version: `1.0.0`
   - Build: `1`

3. **Signing & Capabilities**
   - Select your Team
   - Enable Automatic signing
   - Add capabilities:
     - Background Modes (Bluetooth, VPN)
     - Network Extensions
     - Push Notifications

4. **Info.plist Configuration**
   - Privacy descriptions for:
     - Bluetooth usage
     - Location services
     - Camera access
     - Microphone access

### Step 3: Build & Archive
1. **Select Target Device**
   - Choose "Any iOS Device (arm64)"

2. **Product → Archive**
   - Wait for build completion
   - Verify no errors

3. **Organizer Window**
   - Select your archive
   - Click "Distribute App"

### Step 4: App Store Connect Setup
1. **Create New App**
   - Go to [App Store Connect](https://appstoreconnect.apple.com)
   - Click "+" → "New App"
   - Fill in:
     - Name: "WizNet"
     - Bundle ID: `com.wiznet.app`
     - SKU: `wiznet-ios`
     - User Access: "Full Access"

2. **App Information**
   - Category: "Social Networking"
   - Subcategory: "Social Networking"
   - Content Rights: "No"
   - Age Rating: Complete questionnaire

### Step 5: App Store Listing
1. **App Information**
   - Name: "WizNet - Decentralized Mesh Network"
   - Subtitle: "Private, Secure, Decentralized"
   - Keywords: "mesh,network,privacy,secure,decentralized,bluetooth,vpn"
   - Description: [Use provided marketing copy]

2. **Screenshots**
   - iPhone 6.7" Display: 1290x2796
   - iPhone 6.5" Display: 1242x2688
   - iPhone 5.5" Display: 1242x2208
   - iPad Pro 12.9" Display: 2048x2732

3. **App Icon**
   - 1024x1024 PNG
   - No transparency
   - No rounded corners

### Step 6: Pricing & Availability
1. **Pricing**
   - Price: Free
   - In-App Purchases: Configure subscription tiers

2. **Availability**
   - Countries: Select all or specific regions
   - Release Type: "Manual Release"

### Step 7: Submit for Review
1. **Upload Build**
   - From Xcode Organizer
   - Select "App Store Connect"
   - Upload and wait for processing

2. **Select Build**
   - In App Store Connect
   - Choose your uploaded build
   - Add build notes for reviewers

3. **Submit for Review**
   - Complete all required fields
   - Submit for review
   - Wait 1-7 days for approval

## Google Play Store Submission

### Prerequisites
1. **Google Play Console Account** ($25 one-time fee)
   - Sign up at [play.google.com/console](https://play.google.com/console)
   - Complete account verification

2. **Android Studio** (Latest version)
   - Download from [developer.android.com](https://developer.android.com)

3. **Google Play Services**
   - Ensure app uses latest Google Play Services

### Step 1: Prepare Android App
```bash
# Navigate to Android project
cd /home/kira/Documents/Ghostz/WizNet/mobile-apps/android

# Build release APK
./gradlew assembleRelease

# Or build AAB (preferred)
./gradlew bundleRelease
```

### Step 2: Configure Android Project
1. **build.gradle Configuration**
   ```gradle
   android {
       compileSdkVersion 34
       defaultConfig {
           applicationId "com.wiznet.app"
           minSdkVersion 21
           targetSdkVersion 34
           versionCode 1
           versionName "1.0.0"
       }
   }
   ```

2. **AndroidManifest.xml**
   - Add required permissions
   - Configure activities
   - Set app icon and theme

3. **Signing Configuration**
   - Create keystore for release signing
   - Configure signing in build.gradle

### Step 3: Create Google Play Console Account
1. **Sign Up**
   - Go to [play.google.com/console](https://play.google.com/console)
   - Pay $25 registration fee
   - Complete account setup

2. **Developer Account**
   - Complete personal information
   - Accept developer agreement
   - Set up payment profile

### Step 4: Create App in Play Console
1. **New App**
   - Click "Create app"
   - App name: "WizNet"
   - Default language: English
   - App or game: App
   - Free or paid: Free

2. **App Details**
   - Category: "Social"
   - Tags: "mesh networking, privacy, security"
   - Content rating: Complete questionnaire

### Step 5: Upload App Bundle
1. **Production Track**
   - Go to "Production" track
   - Click "Create new release"
   - Upload AAB file

2. **Release Notes**
   - Add release notes for users
   - Include key features and improvements

### Step 6: Store Listing
1. **App Details**
   - Short description: "Decentralized mesh networking for private, secure communication"
   - Full description: [Use provided marketing copy]
   - Graphics: Screenshots, feature graphic, app icon

2. **Content Rating**
   - Complete content rating questionnaire
   - Get rating certificate

3. **Pricing & Distribution**
   - Price: Free
   - Countries: Select distribution countries
   - Content: Set content guidelines

### Step 7: Submit for Review
1. **Review Information**
   - Add app access instructions
   - Provide test account if needed
   - Add review notes

2. **Submit**
   - Review all sections
   - Submit for review
   - Wait 1-3 days for approval

## Common Requirements for Both Stores

### Legal Compliance
- [x] Privacy Policy (implemented)
- [x] Terms of Service (implemented)
- [x] Data handling compliance
- [x] GDPR compliance (EU)

### Technical Requirements
- [x] No crashes on launch
- [x] Proper error handling
- [x] Accessibility support
- [x] Performance optimization
- [x] Security best practices

### Content Guidelines
- [x] No misleading information
- [x] Appropriate content rating
- [x] Clear app description
- [x] Accurate screenshots

## Post-Submission Checklist

### iOS App Store
- [ ] Monitor review status
- [ ] Respond to reviewer questions
- [ ] Fix any rejection issues
- [ ] Prepare for launch
- [ ] Set up analytics
- [ ] Configure App Store Connect

### Google Play Store
- [ ] Monitor review status
- [ ] Respond to reviewer feedback
- [ ] Fix any rejection issues
- [ ] Prepare for launch
- [ ] Set up Firebase Analytics
- [ ] Configure Play Console

## Launch Strategy

### Pre-Launch
1. **Beta Testing**
   - iOS: TestFlight
   - Android: Internal testing track

2. **Marketing Preparation**
   - Website updates
   - Social media announcements
   - Press release preparation

3. **Support Infrastructure**
   - Customer support system
   - Documentation
   - FAQ preparation

### Launch Day
1. **App Store Optimization**
   - Monitor rankings
   - Track downloads
   - Monitor reviews

2. **Marketing Push**
   - Social media campaign
   - Press outreach
   - Community engagement

3. **Support**
   - Monitor support requests
   - Address issues quickly
   - Gather user feedback

### Post-Launch
1. **Monitoring**
   - Analytics tracking
   - Crash reporting
   - User feedback collection

2. **Updates**
   - Plan regular updates
   - Address user feedback
   - Add new features

3. **Growth**
   - Marketing campaigns
   - User acquisition
   - Retention strategies

## Troubleshooting Common Issues

### iOS Rejections
- **Guideline 2.1**: App crashes
  - Fix: Ensure proper error handling
- **Guideline 4.2**: Minimum functionality
  - Fix: Add more features or improve existing ones
- **Guideline 5.1.1**: Data collection
  - Fix: Update privacy policy and data handling

### Android Rejections
- **Policy Violation**: Inappropriate content
  - Fix: Review and update content
- **Technical Issues**: App crashes
  - Fix: Debug and fix crash issues
- **Metadata Issues**: Misleading information
  - Fix: Update app description and screenshots

## Success Metrics

### Launch Goals
- **Downloads**: 1,000+ first week
- **Reviews**: 4.5+ star rating
- **Retention**: 70% day 1, 30% day 7
- **Engagement**: 5+ minutes average session

### Long-term Goals
- **User Base**: 10,000+ active users
- **Revenue**: $5,000+ monthly recurring
- **Network Effect**: 100+ mesh nodes
- **Community**: Active user community

## Next Steps After Submission

1. **Monitor Review Process**
   - Check status daily
   - Respond to any issues

2. **Prepare Marketing**
   - Website updates
   - Social media content
   - Press outreach

3. **Plan Updates**
   - Feature roadmap
   - Bug fix schedule
   - User feedback integration

4. **Build Community**
   - User forums
   - Discord server
   - Social media presence

This guide ensures a smooth submission process for both app stores with all legal and technical requirements met. 