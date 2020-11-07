---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: 21e1af2a36478f2e0b8e470660d0fbe2539a396e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924009"
---
# <span data-ttu-id="b696a-101">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="b696a-101">Get-AzProviderOperation</span></span>

## <span data-ttu-id="b696a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b696a-102">SYNOPSIS</span></span>
<span data-ttu-id="b696a-103">Hämtar de åtgärder för en Azure-adressresurs som är skyddade med Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="b696a-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

## <span data-ttu-id="b696a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b696a-104">SYNTAX</span></span>

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b696a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b696a-105">DESCRIPTION</span></span>
<span data-ttu-id="b696a-106">Get-AzProviderOperation får de operationer som tillhandahålls av Azure Resource providers.</span><span class="sxs-lookup"><span data-stu-id="b696a-106">The Get-AzProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="b696a-107">Operationer kan skapas för att skapa anpassade roller i Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="b696a-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="b696a-108">Kommandot tar sig en gång i Sök strängen (med möjliga jokertecken ( *)-tecken) som avgör vilka verksamhets uppgifter som ska visas. Använd Get-AzProviderOperation \* för att få alla funktioner för alla Azure Resource-leverantörer. Använd Get-AzProviderOperation Microsoft. Compute/* för att få alla funktioner i Microsoft. Compute Resource Provider.</span><span class="sxs-lookup"><span data-stu-id="b696a-108">The command takes as input an operation search string (with possible wildcard( *) character(s)) which determines the operations details to display. Use Get-AzProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="b696a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b696a-109">EXAMPLES</span></span>

### <span data-ttu-id="b696a-110">Få alla åtgärder för alla providrar</span><span class="sxs-lookup"><span data-stu-id="b696a-110">Get all actions for all providers</span></span>
```
PS C:\> Get-AzProviderOperation *
```

### <span data-ttu-id="b696a-111">Få instruktioner för en viss resurs leverantör</span><span class="sxs-lookup"><span data-stu-id="b696a-111">Get actions for a particular resource provider</span></span>
```
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="b696a-112">Hämta alla åtgärder som kan utföras på virtuella datorer</span><span class="sxs-lookup"><span data-stu-id="b696a-112">Get all actions that can be performed on virtual machines</span></span>
```
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## <span data-ttu-id="b696a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b696a-113">PARAMETERS</span></span>

### <span data-ttu-id="b696a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b696a-114">-DefaultProfile</span></span>
<span data-ttu-id="b696a-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b696a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b696a-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="b696a-116">-OperationSearchString</span></span>
<span data-ttu-id="b696a-117">Sök strängen för åtgärden (med möjliga jokertecken (\*))</span><span class="sxs-lookup"><span data-stu-id="b696a-117">The operation search string (with possible wildcard (\*) characters)</span></span>

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

### <span data-ttu-id="b696a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b696a-118">CommonParameters</span></span>
<span data-ttu-id="b696a-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b696a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b696a-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b696a-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b696a-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b696a-121">INPUTS</span></span>

### <span data-ttu-id="b696a-122">System. String</span><span class="sxs-lookup"><span data-stu-id="b696a-122">System.String</span></span>
<span data-ttu-id="b696a-123">Parametrar: OperationSearchString (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b696a-123">Parameters: OperationSearchString (ByValue)</span></span>

## <span data-ttu-id="b696a-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b696a-124">OUTPUTS</span></span>

### <span data-ttu-id="b696a-125">Microsoft. Azure. commands. Resources. Models. PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="b696a-125">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="b696a-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b696a-126">NOTES</span></span>
<span data-ttu-id="b696a-127">Nyckelord: Azure, AZ, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="b696a-127">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b696a-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b696a-128">RELATED LINKS</span></span>
