SELECT TM.NUMEROMENSAJE, TM.FREAL, TM.CCUENTA, TM.CATEGORIA, TC.DESCRIPCION, TM.DEBITOCREDITO, TM.VALORMONEDACUENTA, TM.RUBRO, TM.CGRUPOBALANCE, TM.CODIGOCONTABLE, TM.CESTATUSCUENTA, TM.CSUBSISTEMA_TRANSACCION,
TM.CTRANSACCION, TM.CSUBSISTEMA_ORIGEN, TM.CTRANSACCION_ORIGEN, TM.CCANAL, TM.CGRUPOPRODUCTO, TM.CPRODUCTO, TM.STRANSACCION, TM.PARTICION, TM.CUSUARIO, TM.CPERSONA_CLIENTE
FROM TMOVIMIENTOS TM
LEFT JOIN TCATEGORIAS TC ON TM.CATEGORIA = TC.CATEGORIA AND TM.CGRUPOBALANCE = TC.CGRUPOBALANCE AND TC.FHASTA > SYSDATE
WHERE CCUENTA = '0209020211' AND
TM.FCONTABLE = '11-11-2026' -- TM.CUSUARIO = 'BA11000342' AND TM.CSUBSISTEMA_CTRANSACCION||TM.CTRANSACCION = '036011' -- AND TM.CATEGORIA IN ('DEPVEF') --AND
--NUMEROMENSAJE = '-28530993a19e7487273fa31bb'
--AND TM.NUMEROCOMPROBANTE = '132882'
ORDER BY FREAL DESC;


select *
from TMOVIMIENTOS where NUMEROMENSAJE ='-42f8cea1a1d029af77a-7cc3';

select *
from tcuentacheques where ccuenta ='0017046950' and numerocheque ='218967';

SELECT * FROM TCUENTACHEQUERASID tci
WHERE tci.CCUENTA = '0017046950';


SELECT * FROM TCUENTACHEQUESLOCALES tchl
WHERE tchl.CUENTAGIRADA = '0017046950'
AND tchl.NUMEROCHEQUE = '218967';



select *
from TCUENTACHEQUES WHERE CCUENTA ='1300626021' AND NUMEROCHEQUE ='14';

update TCUENTACHEQUES set CMOTIVOESTATUSCHEQUE ='1' WHERE CCUENTA ='1300626021' AND NUMEROCHEQUE ='14';


select *   FROM TFEFACTURA   WHERE ESTATUSENVIO='E' AND FECHAEMISION >=TO_DATE('2026-11-10','YYYY-MM-DD');


-- 1) Tipo de ID y cuentas del cliente (cambia :cpersona)
  SELECT tc.ccuenta, tc.cestatuscuenta, tp.CTIPOIDENTIFICACION, tp.identificacion
  FROM TCUENTA tc JOIN TPERSONA tp ON tp.cpersona = tc.cpersona_cliente AND tp.fhasta = FNCFHASTA()
  WHERE tc.cpersona_cliente = '4164772' AND tc.fhasta = FNCFHASTA and CSUBSISTEMA ='04';

  -- 2) Qué ve el query como "utilizado"
  SELECT cal.ccuenta, cal.csubsistema, cal.ctransaccion, cal.freal, cal.montodenominacion, cal.estado
  FROM TCAJACALCULADORA cal
  WHERE cal.ccuenta IN ('0600318985', '2100029033') ORDER BY cal.freal;

  -- 3) Excepciones vigentes
  SELECT ccuenta, montousuario, fmaxima FROM TCUENTAEXCEPCIONES
  WHERE ccuenta IN ('0600318985', '2100029033') AND ctipoexcepcion = 'EBAD' AND fhasta = FNCFHASTA();

  -- 4) Montos y parámetro de la trx 01-9246
  SELECT valortexto natural, valornumerico juridico FROM TCOMPANIAPARAMETROSSISTEMA
  WHERE cparametrosistema = 'MONTOALTADEN' AND fhasta = FNCFHASTA();

SELECT parametro, activado FROM TCOMANDOSMANTENIMIENTO
  WHERE csubsistema = '01' AND ctransaccion = '9246';


  -- Hipótesis 2: relación PRI de ambas cuentas
  SELECT ccuenta, cpersona, crelacionproducto, fhasta
  FROM TCUENTASPERSONA
  WHERE ccuenta IN ('0600318985','2100029033') AND fhasta = FNCFHASTA();

  -- Hipótesis 1: ver si hubo otro depósito con hora cercana (campo de usuario/sesión)
  SELECT ccuenta, ctransaccion, freal, montodenominacion, cusuario, sesion
  FROM TCAJACALCULADORA
  WHERE ccuenta IN ('0600318985','2100029033') AND freal >= DATE '2026-09-14';


select *
from TCAJADETALLEESPECIESMONETARIAS
WHERE NUMEROMENSAJE = '1aceac18a1a0a15aaddbabf9'
      --'-5e04e688a1a0a167ffc2a316b'
    CUSUARIO IN ('BA01260349','BA01190333') AND FCONTABLE ='14-09-2026';

--50   1400  -50  1000
--100  7200  -100 8000
SELECT TM.NUMEROMENSAJE, TM.FREAL, TM.CCUENTA, TM.CATEGORIA, TC.DESCRIPCION, TM.DEBITOCREDITO, TM.VALORMONEDACUENTA, TM.RUBRO, TM.CGRUPOBALANCE, TM.CODIGOCONTABLE, TM.CESTATUSCUENTA, TM.CSUBSISTEMA_TRANSACCION,
TM.CTRANSACCION, TM.CSUBSISTEMA_ORIGEN, TM.CTRANSACCION_ORIGEN, TM.CCANAL, TM.CGRUPOPRODUCTO, TM.CPRODUCTO, TM.STRANSACCION, TM.PARTICION, TM.CUSUARIO, TM.CPERSONA_CLIENTE
FROM TMOVIMIENTOS TM
LEFT JOIN TCATEGORIAS TC ON TM.CATEGORIA = TC.CATEGORIA AND TM.CGRUPOBALANCE = TC.CGRUPOBALANCE AND TC.FHASTA > SYSDATE
WHERE CCUENTA = '2100029033' AND
TM.FCONTABLE = '14-09-2026' -- TM.CUSUARIO = 'BA11000342' AND TM.CSUBSISTEMA_CTRANSACCION||TM.CTRANSACCION = '036011' -- AND TM.CATEGORIA IN ('DEPVEF') --AND
--NUMEROMENSAJE = '-28530993a19e7487273fa31bb'
--AND TM.NUMEROCOMPROBANTE = '132882'
ORDER BY FREAL DESC;

-- ORA-00060: DEADLOCK DETECTED WHILE WAITING FOR RESOURCE
<div align="center">
 <!-- TYPING ANIMATION -->
        <a href="https://github.com/BryanSagbay"> <img
                src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3000&pause=800&color=A78BFA&center=true&vCenter=true&width=600&lines=Software+Engineer;MSc+Artificial+Intelligence;Full+Stack+Developer;Always+building+something+new+%E2%9A%A1"
                alt="Typing SVG" />
        </a>
    </div>
        <br />
    <div align="center">
        <!-- BADGES -->
        <a href="https://www.linkedin.com/in/bryan-sagbay-1b9912267/" target="_blank">
            <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0A66C2"
                alt="LinkedIn" />
        </a>
        <img
            src="https://komarev.com/ghpvc/?username=BryanSagbay&style=for-the-badge&color=7c3aed&label=PROFILE+VIEWS" />
        <img
            src="https://img.shields.io/github/followers/BryanSagbay?style=for-the-badge&color=5b21b6&labelColor=1e1b4b&label=FOLLOWERS" />
    </div>
    <br>
    <br>
    <div align="center">
        <a href="https://skillicons.dev">
            <img
                src="https://skillicons.dev/icons?i=python,java,js,react,angular,flutter,postgres,mysql,mongodb,firebase&theme=dark" />
        </a>
        <a href="https://skillicons.dev">
            <img
                src="https://skillicons.dev/icons?i=redis,tensorflow,pytorch,sklearn,opencv,docker,vercel,git,github,linux&theme=dark" />
        </a>
    </div>
    <!-- FOOTER -->
    <img width="100%"
        src="https://capsule-render.vercel.app/api?type=waving&height=100&color=0:00d2ff,50:3a7bd5,100:9333ea&descAlignY=100&descAlign=100&fontAlign=50&animation=blink&section=footer" />
</div>
