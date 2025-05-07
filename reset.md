## Remove k8s warning
```bash
sed -i 's/\($this->validation_messages\[\] = __(\)/\/\/ \1/' src/System/Requirement/SafeDocumentRoot.php
```
