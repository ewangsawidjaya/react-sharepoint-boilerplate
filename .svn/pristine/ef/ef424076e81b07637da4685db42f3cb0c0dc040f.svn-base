import React from 'react';
import StyledContainer from '../../common/styled-container';
import StyledRow from '../../common/styled-row';
import ImageEditor from '../../common/image-editor';

export default class ItemTableView extends React.Component {
    constructor(props) {
        super(props);

        this.state = {
            image: `${_spPageContextInfo.webAbsoluteUrl}/SiteAssets/Images/RGO.JPG`
        }
    }

    saveImage(dataURL) {
        this.setState({image: dataURL});
    }

    render() {
        return (
            <div>
                <StyledContainer 
                    className='ImageEditorView' 
                    id='ImageEditorView'
                    title='Image Editor'
                    description={(
                        <p>
                            Below is an example of how to use the ImageEditor component.
                        </p>
                    )}
                >
                    <ImageEditor
                        src={this.state.image}
                        width={630}
                        height={815}
                        label=""
                        id="editor-image"
                        saveImage={this.saveImage.bind(this)}
                    />
                </StyledContainer>
                <StyledContainer
                    title="Usage"
                    className="ImageEditorCode"
                >
                    <pre>{code}</pre>
                </StyledContainer>
            </div>
        )
    }
}

const code =
`import React from 'react';
import StyledContainer from '../../common/styled-container';
import StyledRow from '../../common/styled-row';
import ImageEditor from '../../common/image-editor';

export default class ItemTableView extends React.Component {
    constructor(props) {
        super(props);

        this.state = {
            image: _spPageContextInfo.webAbsoluteUrl + "/SiteAssets/Images/RGO.JPG"
        }
    }

    saveImage(dataURL) {
        this.setState({image: dataURL});
    }

    render() {
        return (
            <div>
                <StyledContainer 
                    className='ImageEditorView' 
                    id='ImageEditorView'
                    title='Image Editor'
                >
                    <ImageEditor
                        src={this.state.image}
                        width={630}
                        height={815}
                        label=""
                        id="editor-image"
                        saveImage={(dataUrl) => this.saveImage(dataURL)}
                    />
                </StyledContainer>
            </div>
        )
    }
}`;