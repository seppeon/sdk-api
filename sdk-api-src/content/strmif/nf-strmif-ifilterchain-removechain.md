---
UID: NF:strmif.IFilterChain.RemoveChain
title: IFilterChain::RemoveChain (strmif.h)
description: The RemoveChain method removes every filter in a filter chain from the filter graph.
helpviewer_keywords: ["IFilterChain interface [DirectShow]","RemoveChain method","IFilterChain.RemoveChain","IFilterChain::RemoveChain","IFilterChainRemoveChain","RemoveChain","RemoveChain method [DirectShow]","RemoveChain method [DirectShow]","IFilterChain interface","dshow.ifilterchain_removechain","strmif/IFilterChain::RemoveChain"]
old-location: dshow\ifilterchain_removechain.htm
tech.root: dshow
ms.assetid: a47d2087-5f06-4fce-b573-16935370a34c
ms.date: 4/26/2023
ms.keywords: IFilterChain interface [DirectShow],RemoveChain method, IFilterChain.RemoveChain, IFilterChain::RemoveChain, IFilterChainRemoveChain, RemoveChain, RemoveChain method [DirectShow], RemoveChain method [DirectShow],IFilterChain interface, dshow.ifilterchain_removechain, strmif/IFilterChain::RemoveChain
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFilterChain::RemoveChain
 - strmif/IFilterChain::RemoveChain
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IFilterChain.RemoveChain
---

# IFilterChain::RemoveChain


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). **MediaPlayer** and **IMFMediaEngine** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>RemoveChain</code> method removes every filter in a filter chain from the filter graph.

## -parameters

### -param pStartFilter [in]

A pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface of the filter at the start of the chain.

### -param pEndFilter [in]

A pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface of the filter at the end of the chain. If this parameter is <b>NULL</b>, the method uses the longest possible filter chain that extends downstream from the start filter.

## -returns

Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the failure otherwise.

## -remarks

You can call this method while the graph is running; the method stops the filters in the chain before removing them from the graph.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifilterchain">IFilterChain Interface</a>