## linux同步机制之wait_event和wake_up

wait_event_interruptible():此函数将当前进程状态设置成TASK_INTERRUPTIBLE，然后调用schedule()，schedule()将位于TASK_INTERRUPTIBLE状态的进程从runqueue队列删除，这个进程不在参与调度，除非其它函数将其放入runqueue中，这就是wake_up函数作用