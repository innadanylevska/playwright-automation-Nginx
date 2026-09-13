# 🎯 DemoQA Automation Framework with Playwright


[![Playwright](https://img.shields.io/badge/Playwright-1.57.0-45ba4b?logo=playwright)](https://playwright.dev/)
[![Allure Report](https://img.shields.io/badge/Allure_Report-Click_Here-6b5b95)](https://innadanylevska.github.io/demoQA-automation-Nginx/)

> A comprehensive end-to-end test automation framework built with Playwright and the Page Object Model pattern, featuring automated CI/CD pipelines and beautiful Allure reports.

## 📖 About This Project

This is a real-world automation testing framework I built to demonstrate professional QA engineering practices. It tests the [DemoQA](https://demoqa.com/) website, covering everything from simple form submissions to complex drag-and-drop interactions.

What makes this framework special:
- **Clean Architecture**: Follows the Page Object Model for maintainable, reusable code
- **Automated CI/CD**: Every push triggers tests and generates reports automatically
- **Visual Reports**: Beautiful Allure reports deployed to GitHub Pages
- **Production-Ready**: Includes retry logic, screenshots on failure, and parallel execution

## 🚀 Quick Start

### Prerequisites
- Node.js (v18 or higher)
- npm or yarn

### Installation

```bash
# Clone the repository
git clone https://github.com/mabdulqadirhamza/playwright-automation-Nginx.git
cd playwright-automation-Nginx

# Install dependencies
npm install

# Install Playwright browsers
npx playwright install chromium
```

### Running Tests

```bash
# Run all tests
npm test

# Run tests in headed mode (see the browser)
npm run test:headed

# Run tests in UI mode (interactive)
npm run test:ui

# Generate and view Allure report
npm run allure:report
```

## 📁 Project Structure

```
├── pages/                      # Page Object Models
│   ├── elements/              # Element interaction pages
│   ├── forms/                 # Form pages
│   ├── alerts_frame_windows/  # Alert and window handling
│   ├── widgets_/              # Widget interaction pages
│   ├── interactions/          # Drag-drop, sortable pages
│   └── BasePage.js            # Base page with common methods
├── tests/                      # Test specifications
│   ├── Elements_demoQa/       # Element tests
│   ├── Form_Application/      # Form tests
│   ├── alerts_frame_windows/  # Alert tests
│   ├── widgets_/              # Widget tests
│   └── interactions/          # Interaction tests
├── data/                       # Test data files
├── utils/                      # Utility functions
├── .github/workflows/          # CI/CD pipeline
└── playwright.config.js        # Playwright configuration
```

## 🧪 Test Coverage

This framework covers **40+ test scenarios** across multiple categories:

### ✅ Elements
- Text Box (form inputs, validation)
- Check Box (nested selections)
- Radio Buttons
- Web Tables (CRUD operations)
- Buttons (different click types)
- Links (new tabs, API calls)
- Upload/Download files
- Dynamic Properties

### ✅ Forms
- Practice Form (complete form submission with file upload)

### ✅ Alerts, Frames & Windows
- Browser Windows (tabs, windows)
- Alerts (accept, dismiss, prompt)
- Frames & Nested Frames
- Modal Dialogs

### ✅ Widgets
- Accordian
- Auto Complete
- Date Picker
- Slider
- Progress Bar
- Tabs
- Tool Tips
- Menu
- Select Menu

### ✅ Interactions
- Sortable (drag to reorder)
- Selectable (multi-select)
- Resizable
- Droppable (drag and drop)
- Dragabble (free drag)

## 🔄 CI/CD Pipeline

Every push to `main` triggers:
1. **Install Dependencies** - Sets up Node.js and installs packages
2. **Install Browsers** - Downloads Chromium for testing
3. **Run Tests** - Executes all test suites in parallel
4. **Generate Report** - Creates Allure report with history
5. **Deploy to GitHub Pages** - Publishes report automatically

**View Live Reports**: [https://innadanylevska.github.io/playwright-automation-Nginx/8/index.html]
## 🎨 Features

- **Page Object Model**: Clean separation of test logic and page interactions
- **Parallel Execution**: Tests run concurrently for faster feedback
- **Auto-Retry**: Failed tests retry automatically (2 times on CI)
- **Screenshots**: Captures screenshots on test failures
- **Trace Files**: Records traces for debugging failed tests
- **Allure Reports**: Beautiful, interactive test reports with history
- **GitHub Actions**: Fully automated CI/CD pipeline
- **Cross-Browser Ready**: Configured for Chromium, Firefox, and WebKit

## 🛠️ Technologies Used

- **Playwright** - Modern end-to-end testing framework
- **JavaScript/Node.js** - Programming language
- **Allure** - Test reporting framework
- **GitHub Actions** - CI/CD automation
- **GitHub Pages** - Report hosting

## 📊 Sample Test

```javascript
test('Fill and submit practice form', async ({ page }) => {
  const formPage = new FormApplicationPage(page);
  
  await formPage.goto();
  await formPage.fillFirstName('John');
  await formPage.fillLastName('Doe');
  await formPage.fillEmail('john.doe@example.com');
  await formPage.selectGender('Male');
  await formPage.fillMobile('1234567890');
  await formPage.submitForm();
  
  await expect(formPage.successMessage).toBeVisible();
});
```

## 🤝 Contributing

This is a personal portfolio project, but I'm open to suggestions! Feel free to:
- Open an issue for bugs or improvements
- Fork the repo and submit a pull request
- Share your feedback

## 📝 License

This project is open source and available for learning purposes.

## 👨‍💻 About Me

I'm a QA Engineer:
- Test automation architecture
- CI/CD pipeline design
- Clean code practices
- Modern testing tools and framework
- Nginx

[![GitHub](https://img.shields.io/badge/GitHub-innadanylevska-181717?style=for-the-badge&logo=github)](https://github.com/innadanylevska)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/innadanylevska/)

---
Author https://github.com/mabdulqadirhamza
