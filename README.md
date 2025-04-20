# rn-segmented-tabs

A customizable, animated tab component for **React Native**, supporting gradients, shared reanimated transitions, and flexible styling.

![Alt text](https://github.com/Dhia-Ben-Hamouda/rn-segmented-tabs/blob/main/src/assets/preview.gif)

## 📦 Installation

```bash
npm install rn-segmented-tabs
# or
yarn add rn-segmented-tabs
```

Then install the required peer dependencies:

```bash
npm install react-native-reanimated react-native-linear-gradient
```

---

## ✨ Features

- Animated tab indicator using Reanimated
- Custom tab labels and styles
- Optional linear gradient indicator
- Fully configurable styles
- Controlled component model

---

## 🚀 Usage

```tsx
import Tabs, { ITabOption } from "rn-segmented-tabs";

const tabOptions: ITabOption[] = [
  { label: "Home", value: "home" },
  { label: "Profile", value: "profile" },
  { label: "Settings", value: "settings" },
];

export default function App() {
  const [selectedTab, setSelectedTab] = useState(tabOptions[0]);

  return (
    <Tabs
      options={tabOptions}
      selectedValue={selectedTab}
      onChange={(tab) => {
        setSelectedTab(tab);
      }}
    />
  );
}
```

---

## 🔧 Props

| Prop                  | Type                        | Default            | Description                                |
| --------------------- | --------------------------- | ------------------ | ------------------------------------------ |
| `options`             | `ITabOption[]`              | `undefined`        | List of tabs with `label` and `value`      |
| `selectedValue`       | `ITabOption`                | `undefined`        | Currently selected tab object              |
| `onChange`            | `(tab: ITabOption) => void` | `undefined`        | Callback when tab changes                  |
| `innerPadding`        | `number`                    | `8`                | Padding inside the tab container           |
| `containerStyle`      | `StyleProp<ViewStyle>`      | `undefined`        | Custom styles for the outer container      |
| `labelStyle`          | `StyleProp<TextStyle>`      | `undefined`        | Custom styles for the tab labels           |
| `indicatorStyle`      | `StyleProp<ViewStyle>`      | `undefined`        | Custom styles for the active tab indicator |
| `tabStyle`            | `StyleProp<ViewStyle>`      | `undefined`        | Custom styles for each tab                 |
| `activeTabLabelColor` | `string`                    | `"#000"`           | Label color for the selected tab           |
| `tabLabelColor`       | `string`                    | `"#000"`           | Label color for inactive tabs              |
| `useGradients`        | `boolean`                   | `false`            | Whether to apply gradient to indicator     |
| `gradientColors`      | `string[]`                  | `["#333", "#999"]` | Colors used for gradient indicator         |
| `gradientStart`       | `{ x: number; y: number }`  | `{ x: 0, y: 0 }`   | Gradient start coordinate                  |
| `gradientEnd`         | `{ x: number; y: number }`  | `{ x: 1, y: 0 }`   | Gradient end coordinate                    |
| `animationConfig`     | `WithTimingConfig`          | `undefined`        | Reanimated timing config for transitions   |

## 📦 `ITabOption`

| Prop    | Type     | Default      | Description                      |
| ------- | -------- | ------------ | -------------------------------- |
| `label` | `string` | **required** | Text to display for the option   |
| `value` | `string` | **required** | Value associated with the option |

---

## 📚 Contributing

Issues and pull requests are welcome! Please open an issue first to discuss major changes.

Made with ❤️ by Dhia Ben Hamouda
