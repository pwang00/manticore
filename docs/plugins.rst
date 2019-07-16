Plugins
-------

Core
^^^^

.. py:function:: will_fork_state_callback(self, state, expression, solutions, policy)

.. py:function:: did_fork_state_callback(self, state, new_state, expression, new_value,policy)

.. py:function:: will_load_state_callback(self, state, state_id)

.. py:function:: did_load_state_callback(self, state, state_id)

.. py:function:: will_run_callback(self, state, ready_states)

.. py:function:: did_run_callback(self, state)

Worker
^^^^^^

.. py:function:: will_start_worker_callback(self, state, workerid)

.. py:function:: will_terminate_state_callback(self, state, current_state, exception)

.. py:function:: did_terminate_state_callback(self, state, current_state, exception)

.. py:function:: will_kill_state_callback(self, state, current_state, exception)

.. py:function:: did_sill_state_callback(self, state, current_state, exception)

.. py:function:: did_terminate_worker_callback(self, state, workerid)

EVM
^^^

.. py:function:: will_decode_instruction_callback(self, state, pc)

.. py:function:: will_evm_execute_instruction_callback(self, state, instruction, args)

.. py:function:: did_evm_execute_instruction_callback(self, state, last_unstruction, last_arguments, result)

.. py:function:: did_evm_read_memory_callback(self, state, offset, operators)

.. py:function:: did_evm_write_memory_callback(self, state, offset, operators)

.. py:function:: on_symbolic_sha3_callback(self, state, data, know_sha3)

.. py:function:: on_concreate_sha3_callback(self, state, data, value)

.. py:function:: did_evm_read_code_callback(self, state, code_offset, size)

.. py:function:: will_evm_read_storage_callback(self, state, storage_address, offset)

.. py:function:: did_evm_read_storage_callback(self, state, storage_address, offset, value)

.. py:function:: will_evm_write_storage_callback(self, state, storage_address, offset, value)

.. py:function:: did_evm_write_storage_callback(self, state, storage_address, offset, value)

.. py:function:: will_open_transaction_callback(self, state, tx)

.. py:function:: did_open_transaction_callback(self, state, tx)

.. py:function:: will_close_transaction_callback(self, state, tx)

.. py:function:: did_close_transaction_callback(self, state, tx)

memory
^^^^^^

.. py:function:: will_map_memory_callback(self, state, addr, size, perms, filename, offset)

.. py:function:: did_map_memory_callback(self, state, addr, size, perms, filename, offset, addr) # little confused on this one

.. py:function:: will_map_memory_callback(self, state, addr, size, perms, None, None)

.. py:function:: did_map_memory_callback(self, state, addr, size, perms, None, None, addr)

.. py:function:: will_unmap_memory_callback(self, state, start, size)

.. py:function:: did_unmap_memory_callback(self, state, start, size)

.. py:function:: will_protect_memory_callback(self, state, start, size, perms)

.. py:function:: did_protect_memory_callback(self, state, addr, size, perms, filename, offset)

abstractcpu
^^^^^^^^^^^

.. py:function:: will_execute_syscall_callback(self, state, model)

.. py:function:: did_execute_syscall_callback(self, state, func_name, args, ret)

.. py:function:: will_write_register_callback(self, state, register, value)

.. py:function:: did_write_register_callback(self, state, register, value)

.. py:function:: will_read_register_callback(self, state, register)

.. py:function:: did_read_register_callback(self, state, register, value)

.. py:function:: will_write_memory_callback(self, state, where, expression, size)

.. py:function:: did_write_memory_callback(self, state, where, expression, size)

.. py:function:: will_read_memory_callback(self, state, where, size)

.. py:function:: did_read_memory_callback(self, state, where, size)

.. py:function:: did_write_memory_callback(self, state, where, data, num_bits) # iffy

.. py:function:: will_decode_instruction_callback(self, state, pc)

.. py:function:: will_execute_instruction_callback(self, state, pc, insn)

.. py:function:: did_execute_instruction_callback(self, state, last_pc, pc, insn)

x86
^^^

.. py:function:: will_set_descriptor_callback(self, state, selector, base, limit, perms)

.. py:function:: did_set_descriptor_callback(self, state, selector, base, limit, perms)
