# PHP Coding Standards

## Code Style
- **Standard:** Strictly follow PSR-12.
- **Strict Typing:** ALWAYS add `declare(strict_types=1);` at the top of every PHP file.
- **Type Declarations:** Use explicit types for all properties, arguments, and return values.
    - `public function getTotal(float $price): float`

## Architecture (Laravel/General)
- **SOLID:** Adhere strictly to SOLID principles.
- **Thin Controllers:** Move business logic to Services, Actions, or Jobs. Controllers should only handle request/response.
- **Eloquent:** Use Relationships, Scopes, and Accessors. Avoid raw SQL.
- **DTOs:** Use Data Transfer Objects for passing complex data between layers.

## Testing Patterns
- **Framework:** `Pest PHP` (preferred) or `PHPUnit`.
- **Strategy:** Write feature tests for endpoints and unit tests for complex logic/services.
