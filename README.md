# Лабораторная работа П05: Ansible advanced

**Выполнил:** vsevolodbelonogov (sbelwork@gmail.com)

## Что сделано
1. Использованы 2 виртуальные машины (Control-node и Managed-node, клон Ubuntu2, IP 172.21.235.26).
2. Проверен SSH-доступ на managed-node.
3. Подготовлены файлы: `inventory.ini`, `targets.txt`, `playbook.yml`.
4. `playbook.yml`: установка nmap + сканирование целей из `targets.txt` через `loop` + `register`, вывод `stdout_lines`.
5. Отработаны advanced-механики Ansible:
   - `vars` + `debug`;
   - `loop` по списку;
   - `handlers` + `notify`;
   - Jinja2 template (`templates/test.j2`);
   - Ansible Vault (`secret.yml`, шифрование + `--ask-vault-pass`).

## Файлы
- `inventory.ini`, `targets.txt`, `playbook.yml`;
- `playbook_vars.yml`, `playbook_loops.yml`, `playbook_handler.yml`, `playbook_template.yml`, `playbook_vault.yml`;
- `templates/test.j2`, `secret.yml`;
- `screenshots/` — 10 скриншотов.

## Скриншоты
- `01_two_vms.png` — список WSL-машин (видно 2 машины).
- `02_ssh_check.png` — проверка SSH-доступа на managed-node.
- `03_files_prepared.png` — файлы проекта (`inventory.ini`, `targets.txt`, `playbook.yml`).
- `05_scan_run.png` — запуск nmap через Ansible.
- `06_vars_debug.png` — демонстрация vars + debug.
- `07_loops.png` — демонстрация цикла по списку.
- `08_handlers.png` — срабатывание handler после задачи.
- `09_template.png` — рендер Jinja2-шаблона.
- `10_vault_encrypted.png` — зашифрованный файл `secret.yml`.
- `11_vault_decrypted.png` — успешная расшифровка секрета при запуске плейбука.

## Вывод
Освоены advanced-механики Ansible: переменные, циклы, handlers, register, jinja2, vault.
