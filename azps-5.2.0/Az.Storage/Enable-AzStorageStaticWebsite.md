---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
ms.openlocfilehash: e97e89c1ab7160f1eb06c9c94cd5620a48b0463e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98388950"
---
# <span data-ttu-id="e73a3-101">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e73a3-101">Enable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="e73a3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e73a3-102">SYNOPSIS</span></span>
<span data-ttu-id="e73a3-103">Aktivera statisk webbplats för Azure Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="e73a3-103">Enable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="e73a3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e73a3-104">SYNTAX</span></span>

```
Enable-AzStorageStaticWebsite [[-IndexDocument] <String>] [[-ErrorDocument404Path] <String>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e73a3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e73a3-105">DESCRIPTION</span></span>
<span data-ttu-id="e73a3-106">Cmdleten **Enable-AzStorageStaticWebsite** aktiverar statisk webbplats för Azure Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="e73a3-106">The **Enable-AzStorageStaticWebsite** cmdlet enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="e73a3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e73a3-107">EXAMPLES</span></span>

### <span data-ttu-id="e73a3-108">Exempel 1: aktivera statisk webbplats för Azure Storage-kontot</span><span class="sxs-lookup"><span data-stu-id="e73a3-108">Example 1: Enable static website for the Azure Storage account</span></span>
```
C:\PS>Enable-AzStorageStaticWebsite -IndexDocument $indexdoc -ErrorDocument404Path $errordoc
```

<span data-ttu-id="e73a3-109">Det här kommandot aktiverar statisk webbplats för Azure Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="e73a3-109">This command enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="e73a3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e73a3-110">PARAMETERS</span></span>

### <span data-ttu-id="e73a3-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="e73a3-111">-Context</span></span>
<span data-ttu-id="e73a3-112">Kontext objekt för Azure-lagring</span><span class="sxs-lookup"><span data-stu-id="e73a3-112">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e73a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e73a3-113">-DefaultProfile</span></span>
<span data-ttu-id="e73a3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e73a3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73a3-115">-ErrorDocument404Path</span><span class="sxs-lookup"><span data-stu-id="e73a3-115">-ErrorDocument404Path</span></span>
<span data-ttu-id="e73a3-116">Sökvägen till det fel dokument som ska visas när en 404 utfärdas (d.v.s. När en webbläsare efterfrågar en sida som inte finns.)</span><span class="sxs-lookup"><span data-stu-id="e73a3-116">The path to the error document that should be shown when a 404 is issued (meaning, when a browser requests a page that does not exist.)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73a3-117">-IndexDocument</span><span class="sxs-lookup"><span data-stu-id="e73a3-117">-IndexDocument</span></span>
<span data-ttu-id="e73a3-118">Namnet på index dokumentet i varje katalog.</span><span class="sxs-lookup"><span data-stu-id="e73a3-118">The name of the index document in each directory.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73a3-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e73a3-119">-PassThru</span></span>
<span data-ttu-id="e73a3-120">Visa inställningar för statisk webbplats i ServiceProperties.</span><span class="sxs-lookup"><span data-stu-id="e73a3-120">Display Static Website setting in ServiceProperties.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73a3-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e73a3-121">-Confirm</span></span>
<span data-ttu-id="e73a3-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e73a3-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73a3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e73a3-123">-WhatIf</span></span>
<span data-ttu-id="e73a3-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e73a3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e73a3-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e73a3-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73a3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e73a3-126">CommonParameters</span></span>
<span data-ttu-id="e73a3-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e73a3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e73a3-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e73a3-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e73a3-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e73a3-129">INPUTS</span></span>

### <span data-ttu-id="e73a3-130">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e73a3-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e73a3-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e73a3-131">OUTPUTS</span></span>

### <span data-ttu-id="e73a3-132">Microsoft. WindowsAzure. commands. Storage. Model. ResourceModel. PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="e73a3-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="e73a3-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e73a3-133">NOTES</span></span>

## <span data-ttu-id="e73a3-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e73a3-134">RELATED LINKS</span></span>
