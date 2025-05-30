# Goal Planning Tool (Flutter App)

A comprehensive Goal Planning tool built with Flutter, designed to help users set and achieve long-term financial goals such as retirement, child education, or wealth creation. The app considers inflation, investment growth, and target timelines, allowing users to project future portfolio values using real-time data and compound growth models.

---

## Features

- **Goal Planning**: Set long-term goals with timeline, target amount, and inflation rate.
- **Comprehensive Investment Tracking**:
  - Mutual Funds (real-time data via [MFAPI](https://api.mfapi.in/mf))
  - Stocks (real-time or historical via [Indian Stock Market API](https://indianapi.in/indian-stock-market))
  - Provident Fund (PF)
  - Other Investment types
- **Dynamic Phases**: Collect and project data in three user-defined phases (e.g., 2025-27, 2027-29, 2029-30).
- **Investment Projection**: Visualize future values year-wise and phase-wise using compound growth models.
- **Modern Tab View**: Switch between phases with a dynamic, interactive chart.
- **PDF Export**: Export projection charts and reports as PDF.
- **Responsive Design**: Optimized for tablets and mobile devices.
- **Clean Architecture**: Feature-first folder structure for scalability and maintainability.
- **Test Coverage**: Includes test cases.
- **Latest Flutter SDK**: Built with the latest stable Flutter version.

---

## Screenshots & Figma Design

- [Figma Design Reference](https://www.figma.com/design/TMBe07zbdSLcb41IN25lja/New-Task-File?node-id=1-138&t=UsVKbhrURtgdyLqN-0)

---

## How It Works

### 1. Goal Input Collection

Users provide:
- **Target Year** (e.g., 2030)
- **Target Amount** (e.g., ₹1 Crore)
- **Inflation Rate** (e.g., 4%)

Inputs can be split into three phases (e.g., 2025-27, 2027-29, 2029-30).

### 2. Investment Details

#### Mutual Funds
- Fetch list of mutual funds using [MFAPI](https://api.mfapi.in/mf).
- User selects funds, enters investment amount, category, and SIP for each phase.

#### Stocks
- Get real-time/historical data via [Indian Stock Market API](https://indianapi.in/indian-stock-market) (requires sign-in).
- User enters investments for each phase.

#### Provident Fund (PF)
- User inputs total corpus, annual contribution, and interest rate.
- Projected using compound interest for each phase.

#### Other Investments
- User provides investment type, corpus, and expected annual return rate.

### 3. Investment Projection

- Calculate and display projections year-wise and phase-wise for all investments.
- Interactive chart displays breakdown by investment type and overall progress toward the goal.
- Tab view for each phase, with dynamic chart updates.

### 4. Reports

- Export projection charts as PDF for sharing or record-keeping.

---

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
   cd YOUR-REPO-NAME
   ```

2. **Install dependencies:**
   ```bash
   flutter pub get
   ```

3. **Run the app:**
   ```bash
   flutter run
   ```

4. **Run tests:**
   ```bash
   flutter test
   ```

---

## Folder Structure

```
lib/
│
├── features/
│   ├── goal_input/
│   ├── investments/
│   ├── projections/
│   ├── pdf_export/
│   └── ...
├── core/
├── shared/
├── main.dart
test/
```

- **Feature-first structure:** Each major feature is a separate folder.
- **Core:** Common utilities, services, and base classes.
- **Shared:** Widgets or code used across multiple features.

---

## API Keys & Configuration

- **Mutual Funds:** No key required.
- **Stocks:** Register and obtain API key from [indianapi.in](https://indianapi.in/indian-stock-market).
- **Configuration:** Add your API keys and endpoints in `lib/core/config.dart`.

---

## Roadmap

- [ ] Add user authentication (optional)
- [ ] Add support for new investment types
- [ ] Cloud sync & backup
- [ ] Advanced analytics and goal recommendations

---

## Contributing

1. Fork the repo.
2. Create your feature branch: `git checkout -b feature/YourFeature`.
3. Commit your changes: `git commit -am 'Add some feature'`.
4. Push to the branch: `git push origin feature/YourFeature`.
5. Submit a pull request.

---

## License

[MIT](LICENSE)

---

## Deliverables

- Modern responsive Flutter app (tablet + mobile)
- Clean, scalable codebase with feature-first structure
- Test cases included
- GitHub repository with source code
- Screen recording of app usage

---

**Note:**  
Please refer to the [Figma design](https://www.figma.com/design/TMBe07zbdSLcb41IN25lja/New-Task-File?node-id=1-138&t=UsVKbhrURtgdyLqN-0) for the latest UI/UX specifications and projection chart layout.
