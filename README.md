# @keminghe/node-utils-template

![NPM Version](https://img.shields.io/npm/v/%40keminghe%2Fnode-utils-template)
![NPM License](https://img.shields.io/npm/l/%40keminghe%2Fnode-utils-template)
[![codecov](https://codecov.io/gh/KemingHe/node-utils-template/graph/badge.svg?token=ryf67P7bm9)](https://codecov.io/gh/KemingHe/node-utils-template)

Template for creating TypeScript utility packages for publishing to NPM registry.

## ⭐ Features

- 📝 Full TypeScript support with comprehensive type definitions
- ⚡️ Zero runtime dependencies with 100% test coverage
- 🔄 Automated releases with Git hooks and strict linting

## 📥 Installation

```bash
npm install @keminghe/node-utils-template
```

## 🚀 Usage

### Environment Variable Utility

```typescript
import { env } from '@keminghe/node-utils-template';

// Basic usage
// Throws runtime error if API_KEY is missing or empty
const apiKey: string = env('API_KEY');

// With default value and pattern validation
const port: string = env('PORT', {
  defaultValue: '3000',
  pattern: /^[0-9]+$/
});
```

### String Validation

```typescript
import { isNonEmptyString } from '@keminghe/node-utils-template';

const value = 'hello';
if (isNonEmptyString(value)) {
  // TypeScript knows value is string here
  console.log(value.toUpperCase());
}
```



## ⚙️ Development

```bash
pnpm install  # Install dependencies

pnpm test     # Run tests

pnpm build    # Build package

pnpm verify   # Full verification
```

## 🤝 Contributing

1. Fork the repository to your GitHub account
2. Create a feature branch (`git checkout -b feature/my-update`)
3. Make changes and commit (`git commit`) with Commitizen
4. Push your changes (`git push origin feature/my-update`)
5. Create a Pull Request for code review

## 📄 License

[MIT License](https://github.com/KemingHe/node-utils-template/blob/main/LICENSE)

Copyright 2025 [Keming He](http://linkedin.com/in/keminghe)
