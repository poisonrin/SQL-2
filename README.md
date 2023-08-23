# SQL-2
USE BRAS_ANAMAX

INSERT INTO TBUF(UF, NOMEUF)
VALUES
('AC', 'Acre'),
('AL', 'Alagoas'),
('AP', 'Amapá'),
('AM', 'Amazonas'),
('BA', 'Bahia'),
('CE', 'Ceará'),
('DF', 'Distrito Federal'),
('ES', 'Espírito Santo'),('GO', 'Goiás'),
('MA', 'Maranhão'),
('MT', 'Mato Grosso'),
('MS', 'Mato Grosso do Sul'),
('MG', 'Minas Gerais'),
('PA', 'Pará'),
('PB', 'Paraíba'),
('PR', 'Paraná'),
('PE', 'Pernambuco'),
('PI', 'Piauí'),
('RJ', 'Rio de Janeiro'),
('RN', 'Rio Grande do Norte'),
('RS', 'Rio Grande do Sul'),
('RO', 'Rondônia'),
('RR', 'Roraima'),
('SC', 'Santa Catarina'),
('SP', 'São Paulo'),
('SE', 'Sergipe'),
('TO', 'Tocantins');
SELECT * FROM TBUF;

INSERT INTO tbEQUIPE(SIGLA, EQUIPE, UF)
VALUES
('FLA', 'Flamengo', 'RJ'),
('SAN', 'Santos', 'SP'),
('PAL', 'Palmeiras', 'SP'),
('ATH', 'Atletico-PR', 'PR'),
('SP', 'São Paulo', 'SP'),
('INT', 'Internacional', 'RS'),
('COR', 'Corinthians', 'SP'),
('FOR', 'Fortaleza', 'CE'),
('GOI', 'Goiás', 'GO'),
('ATM', 'Atletico-MG', 'MG'),
('FLU', 'Fluminense', 'RJ'),
('BOT', 'Botafogo', 'MG'),
('CEA', 'Ceará SC', 'CE'),
('AVA', 'Avai', 'SC'),
('ACG', 'Atlético-GO', 'GO'),
('AMG', 'América-MG', 'MG'),
('CFC', 'Coritiba', 'PR'),
('CUI', 'Cuiabá', 'MT'),
('JUV', 'Juventude', 'RS'),
('BGT', 'Bragantino', 'SP');
SELECT * FROM TBEQUIPE;
INSERT INTO tbRESULTADO(SIGLA, VITORIAS, EMPATES, DERROTAS)
VALUES
('FLA', '18', '8', '12'),
('SAN', '12', '11', '15'),
('PAL', '23', '12', '3'),
('ATH', '16', '10', '12'),
('SP', '13', '15', '10'),
('INT', '20', '13', '5'),
('COR', '18', '11', '9'),
('FOR', '15', '10', '13'),
('GOI', '11', '13', '14'),
('ATM', '15', '13', '10'),
('FLU', '21', '7', '10'),
('BOT', '15', '8', '15'),
('CEA', '10', '9', '19'),
('AVA', '3', '11', '24'),
('ACG', '8', '12', '18'),
('AMG', '15', '8', '15'),
('CFC', '12', '6', '20'),
('CUI', '10', '11', '17'),
('JUV', '3', '13', '22'),
('BGT', '11', '11', '16');
SELECT * FROM TBRESULTADO;

ALTER TABLE TBEQUIPE ADD CODIGO INT;
ALTER TABLE TBEQUIPE ALTER COLUMN CODIGO INT;
ALTER TABLE TBEQUIPE DROP COLUMN CODIGO;

UPDATE TBEQUIPE SET CODIGO = 1 WHERE SIGLA = 'BAH'
UPDATE TBEQUIPE SET CODIGO = 2 WHERE SIGLA = 'ATH'
UPDATE TBEQUIPE SET CODIGO = 3 WHERE SIGLA = 'ATM'
UPDATE TBEQUIPE SET CODIGO = 4 WHERE SIGLA = 'AVA'
UPDATE TBEQUIPE SET EQUIPE = 'Bahia' WHERE SIGLA = 'BAH'

DELETE FROM TBEQUIPE WHERE SIGLA = 'AME'
DELETE FROM TBEQUIPE WHERE UF = 'PR'
