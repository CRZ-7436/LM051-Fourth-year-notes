prev_filters = 64
31. for filters in [64] * 3 + [128] * 4 + [256] * 6 + [512] * 3:
32. strides = 1 if filters == prev_filters else 2
33. model.add(ResidualUnit(filters, strides=strides))
34. prev_filters = filters

be able to explain those lines of code

