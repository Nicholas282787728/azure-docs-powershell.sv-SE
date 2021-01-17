---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
ms.openlocfilehash: a7814734f33e0a68fefacf4e465c1834cce17708
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404323"
---
# <span data-ttu-id="7751d-101">Disable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7751d-101">Disable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="7751d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7751d-102">SYNOPSIS</span></span>
<span data-ttu-id="7751d-103">Inaktivera den statiska webbplatsen för Azure Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="7751d-103">Disable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="7751d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7751d-104">SYNTAX</span></span>

```
Disable-AzStorageStaticWebsite [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7751d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7751d-105">DESCRIPTION</span></span>
<span data-ttu-id="7751d-106">Cmdleten **disable-AzStorageStaticWebsite** inaktiverar den statiska webbplatsen för Azure Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="7751d-106">The **Disable-AzStorageStaticWebsite** cmdlet disables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="7751d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7751d-107">EXAMPLES</span></span>

### <span data-ttu-id="7751d-108">Exempel 1: inaktivera statisk webbplats för ett Azure Storage-konto</span><span class="sxs-lookup"><span data-stu-id="7751d-108">Example 1: Disable static website for a Azure Storage account</span></span>
```
C:\PS>Disable-AzStorageStaticWebsite
```

<span data-ttu-id="7751d-109">Det här kommandot inaktiverar den statiska webbplatsen för ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="7751d-109">This command disables static website for a Azure Storage account.</span></span>

## <span data-ttu-id="7751d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7751d-110">PARAMETERS</span></span>

### <span data-ttu-id="7751d-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="7751d-111">-Context</span></span>
<span data-ttu-id="7751d-112">Kontext objekt för Azure-lagring</span><span class="sxs-lookup"><span data-stu-id="7751d-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="7751d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7751d-113">-DefaultProfile</span></span>
<span data-ttu-id="7751d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7751d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7751d-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7751d-115">-PassThru</span></span>
<span data-ttu-id="7751d-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="7751d-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7751d-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7751d-117">-Confirm</span></span>
<span data-ttu-id="7751d-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7751d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7751d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7751d-119">-WhatIf</span></span>
<span data-ttu-id="7751d-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7751d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7751d-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7751d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7751d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7751d-122">CommonParameters</span></span>
<span data-ttu-id="7751d-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7751d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7751d-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7751d-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7751d-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7751d-125">INPUTS</span></span>

### <span data-ttu-id="7751d-126">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7751d-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7751d-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7751d-127">OUTPUTS</span></span>

### <span data-ttu-id="7751d-128">Microsoft. WindowsAzure. commands. Storage. Model. ResourceModel. PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="7751d-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="7751d-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7751d-129">NOTES</span></span>

## <span data-ttu-id="7751d-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7751d-130">RELATED LINKS</span></span>
