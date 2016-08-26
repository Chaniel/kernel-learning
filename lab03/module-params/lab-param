#include <linux/init.h>
#include <linux/module.h>
#include <linux/sched.h>
MODULE_AUTHOR ("firstname lastname");
MODULE_DESCRIPTION ("A very simple loadable module");

static int number = 24601;
static char *word = "blueberry";

module_param (number, int, S_IRUGO);
module_param (word, charp, S_IRUGO);

MODULE_PARM_DESC (number, "A simple integer modifiable parameter");
MODULE_PARM_DESC (word, "A simple string modifiable parameter");

int my_init_module(void)
{
    printk("The module is now loaded\n");
    printk("number=%d word=%s\n", number, word);
/* if you return -1 , the moule can not be loaded.*/
    return 0;
}

module_init(my_init_module);
void my_cleanup_module(void)
{
    printk("The module is now unloaded\n");
}

module_exit(my_cleanup_module);
