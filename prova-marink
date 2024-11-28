SELECT 
    f.nome AS nome_funcionario, 
    m.numero AS numero_mesa, 
    SUM(v.valor_total) AS total_gasto
FROM 
    Funcionario f
JOIN 
    Atendimento a ON f.id = a.funcionario_id
JOIN 
    Mesa m ON a.mesa_numero = m.numero
JOIN 
    Venda v ON m.numero = v.mesa_numero
GROUP BY 
    f.nome, m.numero
ORDER BY 
    f.nome, m.numero; 
    
    SELECT 
    p.nome AS nome_produto, 
    pp.quantidade AS quantidade_consumida,
    m.numero AS numero_mesa
FROM 
    Mesa m
JOIN 
    Pedido pd ON m.numero = pd.mesa_numero
JOIN 
    Pedido_Produto pp ON pd.id = pp.pedido_id
JOIN 
    Produto p ON pp.produto_codigo = p.codigo
WHERE 
    m.numero = 1; 
    
    DELIMITER $$

CREATE PROCEDURE RedefinirStatusMesa(IN mesa_numero INT)
BEGIN
    UPDATE Mesa
    SET status = 'Livre'
    WHERE numero = mesa_numero;
END$$

DELIMITER ;
