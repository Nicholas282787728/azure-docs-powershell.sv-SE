---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: ebb6635cd593e37eedf4a8e70230cbf0f42e0d92
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744895"
---
# <span data-ttu-id="da634-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="da634-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="da634-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="da634-102">SYNOPSIS</span></span>
<span data-ttu-id="da634-103">Uppdaterar en tillgänglighets uppsättning.</span><span class="sxs-lookup"><span data-stu-id="da634-103">Updates an availability set.</span></span>

## <span data-ttu-id="da634-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="da634-104">SYNTAX</span></span>

```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da634-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="da634-105">DESCRIPTION</span></span>
<span data-ttu-id="da634-106">Cmdleten **Update-AzAvailabilitySet** uppdaterar en tillgänglighets uppsättning.</span><span class="sxs-lookup"><span data-stu-id="da634-106">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="da634-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="da634-107">EXAMPLES</span></span>

### <span data-ttu-id="da634-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="da634-108">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="da634-109">Det här kommandot uppdaterar tillgänglighets uppsättningen med namnet "AvSet01" i resurs gruppen med namnet "ResourceGroup01" till en hanterad tillgänglighets uppsättning.</span><span class="sxs-lookup"><span data-stu-id="da634-109">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="da634-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="da634-110">PARAMETERS</span></span>

### <span data-ttu-id="da634-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da634-111">-AsJob</span></span>
<span data-ttu-id="da634-112">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="da634-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="da634-113">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="da634-113">-AvailabilitySet</span></span>
<span data-ttu-id="da634-114">Anger det tillgänglighets objekt som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="da634-114">Specifies the availability set object to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da634-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da634-115">-DefaultProfile</span></span>
<span data-ttu-id="da634-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="da634-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da634-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="da634-117">-Sku</span></span>
<span data-ttu-id="da634-118">Namnet på SKU</span><span class="sxs-lookup"><span data-stu-id="da634-118">The Name of Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da634-119">-Tagg</span><span class="sxs-lookup"><span data-stu-id="da634-119">-Tag</span></span>
<span data-ttu-id="da634-120">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="da634-120">Key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da634-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="da634-121">-Confirm</span></span>
<span data-ttu-id="da634-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="da634-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da634-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da634-123">-WhatIf</span></span>
<span data-ttu-id="da634-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="da634-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da634-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="da634-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da634-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da634-126">CommonParameters</span></span>
<span data-ttu-id="da634-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da634-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da634-128">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da634-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da634-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="da634-129">INPUTS</span></span>

### <span data-ttu-id="da634-130">Microsoft. Azure. commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="da634-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="da634-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="da634-131">OUTPUTS</span></span>

### <span data-ttu-id="da634-132">Microsoft. Azure. commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="da634-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="da634-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="da634-133">NOTES</span></span>

## <span data-ttu-id="da634-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="da634-134">RELATED LINKS</span></span>
