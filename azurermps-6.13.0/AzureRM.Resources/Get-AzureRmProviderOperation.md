---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
ms.openlocfilehash: ff56fc9df0d2303938700d85323a98575d1fb0a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576117"
---
# <span data-ttu-id="29430-101">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="29430-101">Get-AzureRmProviderOperation</span></span>

## <span data-ttu-id="29430-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="29430-102">SYNOPSIS</span></span>
<span data-ttu-id="29430-103">Hämtar de åtgärder för en Azure-adressresurs som är skyddade med Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="29430-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29430-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="29430-104">SYNTAX</span></span>

```
Get-AzureRmProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="29430-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="29430-105">DESCRIPTION</span></span>
<span data-ttu-id="29430-106">Get-AzureRmProviderOperation får de operationer som tillhandahålls av Azure Resource providers.</span><span class="sxs-lookup"><span data-stu-id="29430-106">The Get-AzureRmProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="29430-107">Operationer kan skapas för att skapa anpassade roller i Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="29430-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="29430-108">Kommandot tar sig en gång i Sök strängen (med möjliga jokertecken ( *)-tecken) som avgör vilka verksamhets uppgifter som ska visas. Använd Get-AzureRmProviderOperation \* för att få alla funktioner för alla Azure Resource-leverantörer. Använd Get-AzureRmProviderOperation Microsoft. Compute/* för att få alla funktioner i Microsoft. Compute Resource Provider.</span><span class="sxs-lookup"><span data-stu-id="29430-108">The command takes as input an operation search string (with possible wildcard( *) character(s)) which determines the operations details to display. Use Get-AzureRmProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzureRmProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="29430-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="29430-109">EXAMPLES</span></span>

### <span data-ttu-id="29430-110">Få alla åtgärder för alla providrar</span><span class="sxs-lookup"><span data-stu-id="29430-110">Get all actions for all providers</span></span>
```
PS C:\> Get-AzureRmProviderOperation *
```

### <span data-ttu-id="29430-111">Få instruktioner för en viss resurs leverantör</span><span class="sxs-lookup"><span data-stu-id="29430-111">Get actions for a particular resource provider</span></span>
```
PS C:\> Get-AzureRmProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="29430-112">Hämta alla åtgärder som kan utföras på virtuella datorer</span><span class="sxs-lookup"><span data-stu-id="29430-112">Get all actions that can be performed on virtual machines</span></span>
```
PS C:\> Get-AzureRmProviderOperation */virtualMachines/*
```

## <span data-ttu-id="29430-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="29430-113">PARAMETERS</span></span>

### <span data-ttu-id="29430-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29430-114">-DefaultProfile</span></span>
<span data-ttu-id="29430-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="29430-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29430-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="29430-116">-OperationSearchString</span></span>
<span data-ttu-id="29430-117">Sök strängen för åtgärden (med möjliga jokertecken (\*))</span><span class="sxs-lookup"><span data-stu-id="29430-117">The operation search string (with possible wildcard (\*) characters)</span></span>

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

### <span data-ttu-id="29430-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29430-118">CommonParameters</span></span>
<span data-ttu-id="29430-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29430-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29430-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29430-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29430-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="29430-121">INPUTS</span></span>

### <span data-ttu-id="29430-122">System. String</span><span class="sxs-lookup"><span data-stu-id="29430-122">System.String</span></span>
<span data-ttu-id="29430-123">Parametrar: OperationSearchString (ByValue)</span><span class="sxs-lookup"><span data-stu-id="29430-123">Parameters: OperationSearchString (ByValue)</span></span>

## <span data-ttu-id="29430-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="29430-124">OUTPUTS</span></span>

### <span data-ttu-id="29430-125">Microsoft. Azure. commands. Resources. Models. PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="29430-125">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="29430-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="29430-126">NOTES</span></span>
<span data-ttu-id="29430-127">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="29430-127">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="29430-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="29430-128">RELATED LINKS</span></span>
