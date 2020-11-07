---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermprovideroperation
schema: 2.0.0
ms.openlocfilehash: 1274b04ed85917a9c1e185bfbef6307eaedecc05
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930078"
---
# <span data-ttu-id="5bbd4-101">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="5bbd4-101">Get-AzureRmProviderOperation</span></span>

## <span data-ttu-id="5bbd4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5bbd4-102">SYNOPSIS</span></span>
<span data-ttu-id="5bbd4-103">Hämtar de åtgärder för en Azure-adressresurs som är skyddade med Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="5bbd4-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bbd4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5bbd4-104">SYNTAX</span></span>

```
Get-AzureRmProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5bbd4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5bbd4-105">DESCRIPTION</span></span>
<span data-ttu-id="5bbd4-106">Get-AzureRmProviderOperation får de operationer som tillhandahålls av Azure Resource providers.</span><span class="sxs-lookup"><span data-stu-id="5bbd4-106">The Get-AzureRmProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="5bbd4-107">Operationer kan skapas för att skapa anpassade roller i Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="5bbd4-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="5bbd4-108">Kommandot tar sig en gång i Sök strängen (med möjliga jokertecken ( *)-tecken) som avgör vilka verksamhets uppgifter som ska visas. Använd Get-AzureRmProviderOperation \* för att få alla funktioner för alla Azure Resource-leverantörer. Använd Get-AzureRmProviderOperation Microsoft. Compute/* för att få alla funktioner i Microsoft. Compute Resource Provider.</span><span class="sxs-lookup"><span data-stu-id="5bbd4-108">The command takes as input an operation search string (with possible wildcard( *) character(s)) which determines the operations details to display. Use Get-AzureRmProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzureRmProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="5bbd4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5bbd4-109">EXAMPLES</span></span>

### <span data-ttu-id="5bbd4-110">Få alla åtgärder för alla providrar</span><span class="sxs-lookup"><span data-stu-id="5bbd4-110">Get all actions for all providers</span></span>
```
PS C:\> Get-AzureRmProviderOperation *
```

### <span data-ttu-id="5bbd4-111">Få instruktioner för en viss resurs leverantör</span><span class="sxs-lookup"><span data-stu-id="5bbd4-111">Get actions for a particular resource provider</span></span>
```
PS C:\> Get-AzureRmProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="5bbd4-112">Hämta alla åtgärder som kan utföras på virtuella datorer</span><span class="sxs-lookup"><span data-stu-id="5bbd4-112">Get all actions that can be performed on virtual machines</span></span>
```
PS C:\> Get-AzureRmProviderOperation */virtualMachines/*
```

## <span data-ttu-id="5bbd4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5bbd4-113">PARAMETERS</span></span>

### <span data-ttu-id="5bbd4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bbd4-114">-DefaultProfile</span></span>
<span data-ttu-id="5bbd4-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5bbd4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bbd4-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="5bbd4-116">-OperationSearchString</span></span>
<span data-ttu-id="5bbd4-117">Sök strängen för åtgärden (med möjliga jokertecken (\*))</span><span class="sxs-lookup"><span data-stu-id="5bbd4-117">The operation search string (with possible wildcard (\*) characters)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bbd4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bbd4-118">CommonParameters</span></span>
<span data-ttu-id="5bbd4-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bbd4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bbd4-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bbd4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bbd4-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5bbd4-121">INPUTS</span></span>

### <span data-ttu-id="5bbd4-122">System. String</span><span class="sxs-lookup"><span data-stu-id="5bbd4-122">System.String</span></span>
<span data-ttu-id="5bbd4-123">Parametrar: OperationSearchString (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5bbd4-123">Parameters: OperationSearchString (ByValue)</span></span>

## <span data-ttu-id="5bbd4-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5bbd4-124">OUTPUTS</span></span>

### <span data-ttu-id="5bbd4-125">Microsoft. Azure. commands. Resources. Models. PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="5bbd4-125">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="5bbd4-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5bbd4-126">NOTES</span></span>
<span data-ttu-id="5bbd4-127">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="5bbd4-127">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="5bbd4-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5bbd4-128">RELATED LINKS</span></span>
