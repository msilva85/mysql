# mysql
Proyecto banco con histórico de movimientos

Para terminos de historicos muchas vecez necesitamos registrar el movimiento, fecha el valor anterior antes de actualizar los datos
por terminos de integridad o tener un respaldo para restarurar los cambios, esto pretende este codigo

#Recuerden crear la base de datos o schema banco

CREATE DATABASE banco;

#exportar archivo a base de datos

mysql -u root -p banco < banco.sql

#respaldar saldo de la tabla cuenta

el trigger movimiento_BEFORE_INSERT, respalda el saldo en la tabla movimiento 

#actualizar saldo de la tabla cliente sea ingreso o egreso, o negativo o positivo

el trigger movimiento_AFTER_INSERT, registra el tipo de movimiento el monto y la fecha y actualiza el saldo en la tabla cliente
