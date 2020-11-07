---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
ms.openlocfilehash: d4e58e1fc2da68d9293afa27072a4cf32023f661
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756564"
---
# <span data-ttu-id="5841e-101">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="5841e-101">Get-AzureRmProviderOperation</span></span>

## <span data-ttu-id="5841e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5841e-102">SYNOPSIS</span></span>
<span data-ttu-id="5841e-103">Hämtar de åtgärder för en Azure-adressresurs som är skyddade med Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="5841e-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5841e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5841e-104">SYNTAX</span></span>

```
Get-AzureRmProviderOperation [-OperationSearchString] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5841e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5841e-105">DESCRIPTION</span></span>
<span data-ttu-id="5841e-106">Get-AzureRmProviderOperation får de operationer som tillhandahålls av Azure Resource providers.</span><span class="sxs-lookup"><span data-stu-id="5841e-106">The Get-AzureRmProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="5841e-107">Operationer kan skapas för att skapa anpassade roller i Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="5841e-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="5841e-108">Kommandot tar sig en gång i Sök strängen (med möjligt jokertecken (\*) tecken som avgör vilka verksamhets uppgifter som ska visas.</span><span class="sxs-lookup"><span data-stu-id="5841e-108">The command takes as input an operation search string (with possible wildcard(\*) character(s)) which determines the operations details to display.</span></span>

<span data-ttu-id="5841e-109">Använd Get-AzureRmProviderOperation \* för att få alla funktioner för alla Azure Resource-leverantörer.</span><span class="sxs-lookup"><span data-stu-id="5841e-109">Use Get-AzureRmProviderOperation \* to get all operations for all Azure resource providers.</span></span>

<span data-ttu-id="5841e-110">Använd Get-AzureRmProviderOperation Microsoft. Compute/\* för att få alla funktioner i Microsoft. Compute Resource Provider.</span><span class="sxs-lookup"><span data-stu-id="5841e-110">Use Get-AzureRmProviderOperation Microsoft.Compute/\* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="5841e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5841e-111">EXAMPLES</span></span>

### <span data-ttu-id="5841e-112">--------------------------Få alla åtgärder--------------------------</span><span class="sxs-lookup"><span data-stu-id="5841e-112">--------------------------  Get all actions for all providers  --------------------------</span></span>
```
PS C:\> Get-AzureRmProviderOperation *
```

### <span data-ttu-id="5841e-113">--------------------------Få instruktioner för en viss resurs leverantör--------------------------</span><span class="sxs-lookup"><span data-stu-id="5841e-113">--------------------------  Get actions for a particular resource provider  --------------------------</span></span>
```
PS C:\> Get-AzureRmProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="5841e-114">--------------------------Få alla åtgärder som kan utföras på virtuella datorer--------------------------</span><span class="sxs-lookup"><span data-stu-id="5841e-114">--------------------------  Get all actions that can be performed on virtual machines  --------------------------</span></span>
```
PS C:\> Get-AzureRmProviderOperation */virtualMachines/*
```

## <span data-ttu-id="5841e-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5841e-115">PARAMETERS</span></span>

### <span data-ttu-id="5841e-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="5841e-116">-OperationSearchString</span></span>
<span data-ttu-id="5841e-117">Sök strängen för åtgärden (med möjliga jokertecken (\*))</span><span class="sxs-lookup"><span data-stu-id="5841e-117">The operation search string (with possible wildcard (\*) characters)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5841e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5841e-118">-DefaultProfile</span></span>
<span data-ttu-id="5841e-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5841e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5841e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5841e-120">CommonParameters</span></span>
<span data-ttu-id="5841e-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5841e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5841e-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5841e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5841e-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5841e-123">INPUTS</span></span>

### <span data-ttu-id="5841e-124">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="5841e-124">String</span></span>
<span data-ttu-id="5841e-125">Parametern ' OperationSearchString ' godkänner värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="5841e-125">Parameter 'OperationSearchString' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="5841e-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5841e-126">OUTPUTS</span></span>

### <span data-ttu-id="5841e-127">Microsoft. Azure. commands. Resources. Models. PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="5841e-127">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="5841e-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5841e-128">NOTES</span></span>
<span data-ttu-id="5841e-129">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="5841e-129">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="5841e-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5841e-130">RELATED LINKS</span></span>

