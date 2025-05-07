## Remove k8s warning
```bash
sed -i 's/\($this->validation_messages\[\] = __(\)/\/\/ \1/' src/System/Requirement/SafeDocumentRoot.php
```
## Enable PVC
- Edit the Deployment.yaml
```bash
volumeMounts:
            {{- if .Values.persistence.enabled }}
            - name: glpi-storage
              mountPath: {{ .Values.persistence.mountPath | default "/var/www/html" }}
            {{- end }}
      volumes:
        {{- if .Values.persistence.enabled }}
        - name: glpi-storage
          persistentVolumeClaim:
            claimName: {{ .Values.persistence.existingClaim }}
        {{- end }}
```
