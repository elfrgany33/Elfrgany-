import React from 'react';
import { Container, Row, Col, Input, Button } from 'react-materialize';

const RegistrationForm = () => {
  return (
    <Container>
      <Row>
        <Col s={12} m={6}>
          <h2>استمارة التسجيل</h2>
          <form>
            <div className="input-field">
              <input id="name" type="text" className="validate" />
              <label for="name">الاسم الكامل</label>
            </div>
            {/* باقي الحقول */}
            <button className="waves-effect waves-light btn">تسجيل</button>
          </form>
        </Col>
      </Row>
    </Container>
  );
};
