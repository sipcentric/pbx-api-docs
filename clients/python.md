# Python

Project home and source code over on [GitHub](https://github.com/sipcentric/sc-lib-python)

## Install

### Best method

    sudo pip install sipcentric

### Manual method

    git clone git@github.com:sipcentric/sc-lib-python.git && cd sc-lib-python
    sudo python setup.py install

## Examples

    import sipcentric
    sms = sipcentric.sms(username="",password="")
    print sms.send(originator="0123", recipient="01212854400", message="Hello World!")
