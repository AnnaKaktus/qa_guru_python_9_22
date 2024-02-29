Запуск appium в терминале - с ключом (команда appium  --base-path /wd/hub)
Менять контекст можно как в самом коде, проставляя в config.py config = Config(context="" и в фикстуре значение default:
def pytest_addoption(parser):
    parser.addoption(
        "--context",
        required=False,
        default="",
        choices=["bstack", "local_real", "local_emulator"],
так и через командную строку (команда pytest tests/ --context {})
