---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
ms.openlocfilehash: e97e89c1ab7160f1eb06c9c94cd5620a48b0463e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269249"
---
# <span data-ttu-id="8c69b-101">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="8c69b-101">Enable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="8c69b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8c69b-102">SYNOPSIS</span></span>
<span data-ttu-id="8c69b-103">Aktivera statisk webbplats för Azure Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="8c69b-103">Enable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="8c69b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8c69b-104">SYNTAX</span></span>

```
Enable-AzStorageStaticWebsite [[-IndexDocument] <String>] [[-ErrorDocument404Path] <String>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8c69b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8c69b-105">DESCRIPTION</span></span>
<span data-ttu-id="8c69b-106">Cmdleten **Enable-AzStorageStaticWebsite** aktiverar statisk webbplats för Azure Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="8c69b-106">The **Enable-AzStorageStaticWebsite** cmdlet enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="8c69b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8c69b-107">EXAMPLES</span></span>

### <span data-ttu-id="8c69b-108">Exempel 1: aktivera statisk webbplats för Azure Storage-kontot</span><span class="sxs-lookup"><span data-stu-id="8c69b-108">Example 1: Enable static website for the Azure Storage account</span></span>
```
C:\PS>Enable-AzStorageStaticWebsite -IndexDocument $indexdoc -ErrorDocument404Path $errordoc
```

<span data-ttu-id="8c69b-109">Det här kommandot aktiverar statisk webbplats för Azure Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="8c69b-109">This command enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="8c69b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8c69b-110">PARAMETERS</span></span>

### <span data-ttu-id="8c69b-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="8c69b-111">-Context</span></span>
<span data-ttu-id="8c69b-112">Kontext objekt för Azure-lagring</span><span class="sxs-lookup"><span data-stu-id="8c69b-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="8c69b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c69b-113">-DefaultProfile</span></span>
<span data-ttu-id="8c69b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8c69b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c69b-115">-ErrorDocument404Path</span><span class="sxs-lookup"><span data-stu-id="8c69b-115">-ErrorDocument404Path</span></span>
<span data-ttu-id="8c69b-116">Sökvägen till det fel dokument som ska visas när en 404 utfärdas (d.v.s. När en webbläsare efterfrågar en sida som inte finns.)</span><span class="sxs-lookup"><span data-stu-id="8c69b-116">The path to the error document that should be shown when a 404 is issued (meaning, when a browser requests a page that does not exist.)</span></span>

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

### <span data-ttu-id="8c69b-117">-IndexDocument</span><span class="sxs-lookup"><span data-stu-id="8c69b-117">-IndexDocument</span></span>
<span data-ttu-id="8c69b-118">Namnet på index dokumentet i varje katalog.</span><span class="sxs-lookup"><span data-stu-id="8c69b-118">The name of the index document in each directory.</span></span>

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

### <span data-ttu-id="8c69b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c69b-119">-PassThru</span></span>
<span data-ttu-id="8c69b-120">Visa inställningar för statisk webbplats i ServiceProperties.</span><span class="sxs-lookup"><span data-stu-id="8c69b-120">Display Static Website setting in ServiceProperties.</span></span>

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

### <span data-ttu-id="8c69b-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8c69b-121">-Confirm</span></span>
<span data-ttu-id="8c69b-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8c69b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c69b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c69b-123">-WhatIf</span></span>
<span data-ttu-id="8c69b-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8c69b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c69b-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8c69b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c69b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c69b-126">CommonParameters</span></span>
<span data-ttu-id="8c69b-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c69b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c69b-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c69b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c69b-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8c69b-129">INPUTS</span></span>

### <span data-ttu-id="8c69b-130">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8c69b-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8c69b-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8c69b-131">OUTPUTS</span></span>

### <span data-ttu-id="8c69b-132">Microsoft. WindowsAzure. commands. Storage. Model. ResourceModel. PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="8c69b-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="8c69b-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8c69b-133">NOTES</span></span>

## <span data-ttu-id="8c69b-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8c69b-134">RELATED LINKS</span></span>
