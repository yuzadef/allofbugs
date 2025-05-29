# business logic flaw

1. **bypass email confirmation for ATO via race condition*** -- attacker change accountA to victim's email; need to confirm the email sent to victim to achieve ATO; race condition confuses the application and send the confirmation link to both attacker and victim; allows attacker to achieve the ATO with zero-click.