# Changelog

All notable changes to this project are documented here.
Format based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [Unreleased]

### Added — Phase 1: Foundation

- Project scaffold with clean, modular architecture (`core/`, `models/`,
  `engines/`, `features/`, `widgets/`).
- Precision-safe expression engine: tokenizer, recursive-descent parser,
  AST, and `ExpressionEvaluator`, built on exact `Rational` arithmetic.
- Smart, context-aware percentage handling (`500 + 10%` vs `500 × 10%`).
- Standalone `PercentageEngine` for non-inline percentage math (discount,
  markup, margin, percent change) for later reuse by the Finance module.
- `NumberFormatter`: thousands separators and trailing-zero trimming
  without ever converting through `double`.
- `CalculatorEngine`: input handling (digit/operator/decimal/percent/
  parens), backspace, clear/clear-all, evaluation, session tape, and
  long-press-equals "repeat last operation".
- Material 3 light/dark/system theme.
- Basic calculator screen: expression + result display, peek handle
  (visual placeholder for Phase 2's Quick Scan), and the four-row keypad.
- Unit tests for the expression evaluator, calculator engine, percentage
  engine, and number formatter, covering the arithmetic/percentage/
  decimal-precision/error-handling scenarios from the product spec.
