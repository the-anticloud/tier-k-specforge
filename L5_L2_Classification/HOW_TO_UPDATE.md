# How to Update — K_SPECFORGE
**Platform:** Anticloud | **IP:** USPTO pending 2026, Anticloud FZ LLE, 0-1.gg

## Module: K_SPECFORGE
Domain: Speculative execution forge: parallel hypothesis generation for PAX 27B multi-path reasoning


## Update Procedure
1. Backup current state
2. Test in api-oss-labs sandbox
3. `pip install --upgrade anticloud-k_specforge`
4. `python -m k_specforge.tests.smoke`
5. `aioss verify --chain ./k_specforge.aioss`
6. Monitor 30 min via api-oss-monitor

## Rollback
```bash
pip install anticloud-k_specforge==<previous>
python -m api_oss_backup restore --archive ./backups/<latest>
```

## Weight Updates
PAX 27B weight updates are signed by Anticloud FZ LLE:
```bash
anticloud tool verify-weights --model ./pax-27b-q4-new.gguf --sig ./pax-27b-q4-new.sig
```
