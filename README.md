# Flycheck checker for PHP using [Noverify](https://github.com/VKCOM/noverify) linter

Noverify - Pretty fast linter (code static analysis utility) for PHP

## Installation

From MELPA:
```
M-x package-install flycheck-php-noverify
```

For `use-package` user:

```elisp
(use-package flycheck-php-noverify
  :ensure t
  :config
  (progn
    (flycheck-php-noverify-setup)))
```

## Configuration

```elisp
;; Excluded checks. 
;; default: '("undefinedConstant" "undefinedClass" "undefinedFunction" 
;;            "undefinedMethod" "undefinedProperty" "undefinedTrait")
(add-to-list 'flycheck-php-noverify-exclude-checks "constCase")
;; Allowed checks. default: nil
(setq flycheck-php-noverify-allow-checks '("unused"))
;; Analyze as PHP 7. default: nil
(setq flycheck-php-noverify-php7 t)
;; additional 'noverify' args
(setq flycheck-php-noverify-args '("--cores" "4"))
