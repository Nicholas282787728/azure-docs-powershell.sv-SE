---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
ms.openlocfilehash: 4d72be4f7ddbe6cd5884269c724c7505cc05fffc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744266"
---
# <span data-ttu-id="d1f4f-101">Get-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="d1f4f-101">Get-AzEventGridDomainKey</span></span>

## <span data-ttu-id="d1f4f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d1f4f-102">SYNOPSIS</span></span>
<span data-ttu-id="d1f4f-103">Hämtar de delade åtkomst nycklarna som används för att publicera händelser till en händelse i en rutnäts domän.</span><span class="sxs-lookup"><span data-stu-id="d1f4f-103">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="d1f4f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d1f4f-104">SYNTAX</span></span>

### <span data-ttu-id="d1f4f-105">DomainNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d1f4f-105">DomainNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1f4f-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1f4f-106">DomainInputObjectParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainObject] <PSDomain> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1f4f-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1f4f-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1f4f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d1f4f-108">DESCRIPTION</span></span>
<span data-ttu-id="d1f4f-109">Hämtar de delade åtkomst nycklarna som används för att publicera händelser till en händelse i en rutnäts domän.</span><span class="sxs-lookup"><span data-stu-id="d1f4f-109">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="d1f4f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d1f4f-110">EXAMPLES</span></span>

### <span data-ttu-id="d1f4f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d1f4f-111">Example 1</span></span>

<span data-ttu-id="d1f4f-112">Hämtar de delade åtkomst nycklarna för händelse rutnät för \` domain1 \` i resurs grupps \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="d1f4f-112">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -Name Domain1

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

### <span data-ttu-id="d1f4f-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d1f4f-113">Example 2</span></span>

<span data-ttu-id="d1f4f-114">Hämtar de delade åtkomst nycklarna för händelse rutnät för \` domain1 \` i resurs grupps \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="d1f4f-114">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | Get-AzEventGridDomainKey

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

## <span data-ttu-id="d1f4f-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d1f4f-115">PARAMETERS</span></span>

### <span data-ttu-id="d1f4f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1f4f-116">-DefaultProfile</span></span>
<span data-ttu-id="d1f4f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d1f4f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f4f-118">-DomainObject</span><span class="sxs-lookup"><span data-stu-id="d1f4f-118">-DomainObject</span></span>
<span data-ttu-id="d1f4f-119">EventGrid.</span><span class="sxs-lookup"><span data-stu-id="d1f4f-119">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: DomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1f4f-120">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="d1f4f-120">-DomainResourceId</span></span>
<span data-ttu-id="d1f4f-121">Resurs-ID som representerar händelse rutnäts domänen.</span><span class="sxs-lookup"><span data-stu-id="d1f4f-121">Resource Identifier representing the Event Grid Domain.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1f4f-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="d1f4f-122">-Name</span></span>
<span data-ttu-id="d1f4f-123">EventGrid domän namn.</span><span class="sxs-lookup"><span data-stu-id="d1f4f-123">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f4f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1f4f-124">-ResourceGroupName</span></span>
<span data-ttu-id="d1f4f-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d1f4f-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f4f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1f4f-126">CommonParameters</span></span>
<span data-ttu-id="d1f4f-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1f4f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1f4f-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1f4f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1f4f-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d1f4f-129">INPUTS</span></span>

### <span data-ttu-id="d1f4f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d1f4f-130">System.String</span></span>

### <span data-ttu-id="d1f4f-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="d1f4f-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="d1f4f-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d1f4f-132">OUTPUTS</span></span>

### <span data-ttu-id="d1f4f-133">Microsoft. Azure. Management. EventGrid. Models. DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="d1f4f-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="d1f4f-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d1f4f-134">NOTES</span></span>

## <span data-ttu-id="d1f4f-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d1f4f-135">RELATED LINKS</span></span>