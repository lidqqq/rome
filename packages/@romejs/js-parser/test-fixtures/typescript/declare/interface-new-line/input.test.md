# `index.test.ts`

**DO NOT MODIFY**. This file has been autogenerated. Run `rome test packages/@romejs/js-parser/index.test.ts --update-snapshots` to update.

## `typescript > declare > interface-new-line`

```javascript
Program {
  comments: Array []
  corrupt: false
  diagnostics: Array []
  directives: Array []
  filename: 'input.ts'
  hasHoistedVars: false
  interpreter: undefined
  mtime: undefined
  sourceType: 'module'
  syntax: Array ['ts']
  loc: Object {
    filename: 'input.ts'
    end: Object {
      column: 0
      index: 23
      line: 3
    }
    start: Object {
      column: 0
      index: 0
      line: 1
    }
  }
  body: Array [
    ExpressionStatement {
      loc: Object {
        filename: 'input.ts'
        end: Object {
          column: 7
          index: 7
          line: 1
        }
        start: Object {
          column: 0
          index: 0
          line: 1
        }
      }
      expression: ReferenceIdentifier {
        name: 'declare'
        loc: Object {
          filename: 'input.ts'
          end: Object {
            column: 7
            index: 7
            line: 1
          }
          start: Object {
            column: 0
            index: 0
            line: 1
          }
        }
      }
    }
    TSInterfaceDeclaration {
      id: BindingIdentifier {
        name: 'I'
        loc: Object {
          filename: 'input.ts'
          end: Object {
            column: 11
            index: 19
            line: 2
          }
          start: Object {
            column: 10
            index: 18
            line: 2
          }
        }
      }
      extends: undefined
      typeParameters: undefined
      loc: Object {
        filename: 'input.ts'
        end: Object {
          column: 14
          index: 22
          line: 2
        }
        start: Object {
          column: 0
          index: 8
          line: 2
        }
      }
      body: TSInterfaceBody {
        body: Array []
        loc: Object {
          filename: 'input.ts'
          end: Object {
            column: 14
            index: 22
            line: 2
          }
          start: Object {
            column: 12
            index: 20
            line: 2
          }
        }
      }
    }
  ]
}
```
