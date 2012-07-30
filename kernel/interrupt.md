MACHINE_START
	.init_irq   = apollo_init_irq,
		apollo_init_irq
			gic_dist_init
			gic_cpu_init
