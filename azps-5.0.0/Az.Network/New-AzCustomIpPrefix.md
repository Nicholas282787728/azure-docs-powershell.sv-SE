---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
ms.openlocfilehash: 08df4120e762a7837376af7413504a8fce678230
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271779"
---
# <span data-ttu-id="c8bbe-101">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c8bbe-101">New-AzCustomIpPrefix</span></span>

## <span data-ttu-id="c8bbe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c8bbe-102">SYNOPSIS</span></span>
<span data-ttu-id="c8bbe-103">Skapar en CustomIpPrefix-resurs</span><span class="sxs-lookup"><span data-stu-id="c8bbe-103">Creates a CustomIpPrefix resource</span></span>

## <span data-ttu-id="c8bbe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c8bbe-104">SYNTAX</span></span>

```
New-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> -Location <String> -Cidr <String>
 [-Zone <String[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c8bbe-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c8bbe-105">DESCRIPTION</span></span>
<span data-ttu-id="c8bbe-106">Cmdleten **New-AzCustomIpPrefix** skapar en CustomIpPrefix-resurs.</span><span class="sxs-lookup"><span data-stu-id="c8bbe-106">The **New-AzCustomIpPrefix** cmdlet creates a CustomIpPrefix resource.</span></span>

## <span data-ttu-id="c8bbe-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c8bbe-107">EXAMPLES</span></span>

### <span data-ttu-id="c8bbe-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c8bbe-108">Example 1</span></span>
```powershell
PS C:\> $myCustomIpPrefix = New-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Cidr 40.40.40.0/24 -Location westus
```

<span data-ttu-id="c8bbe-109">Det här kommandot skapar en ny CustomIpPrefix-resurs med namnet $prefixName i resurs gruppen $rgName med en CIDR på 40.40.40.0/24 under västkusten</span><span class="sxs-lookup"><span data-stu-id="c8bbe-109">This command creates a new CustomIpPrefix resource with name $prefixName in resource group $rgName with a cidr of 40.40.40.0/24 in westus</span></span>

## <span data-ttu-id="c8bbe-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c8bbe-110">PARAMETERS</span></span>

### <span data-ttu-id="c8bbe-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8bbe-111">-AsJob</span></span>
<span data-ttu-id="c8bbe-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="c8bbe-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8bbe-113">-CIDR</span><span class="sxs-lookup"><span data-stu-id="c8bbe-113">-Cidr</span></span>
<span data-ttu-id="c8bbe-114">CustomIpPrefix CIDR.</span><span class="sxs-lookup"><span data-stu-id="c8bbe-114">The CustomIpPrefix CIDR.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8bbe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8bbe-115">-DefaultProfile</span></span>
<span data-ttu-id="c8bbe-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c8bbe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8bbe-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="c8bbe-117">-Location</span></span>
<span data-ttu-id="c8bbe-118">CustomIpPrefix-platsen.</span><span class="sxs-lookup"><span data-stu-id="c8bbe-118">The CustomIpPrefix location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8bbe-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="c8bbe-119">-Name</span></span>
<span data-ttu-id="c8bbe-120">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="c8bbe-120">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8bbe-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8bbe-121">-ResourceGroupName</span></span>
<span data-ttu-id="c8bbe-122">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="c8bbe-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8bbe-123">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c8bbe-123">-Tag</span></span>
<span data-ttu-id="c8bbe-124">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="c8bbe-124">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8bbe-125">-Zone</span><span class="sxs-lookup"><span data-stu-id="c8bbe-125">-Zone</span></span>
<span data-ttu-id="c8bbe-126">En lista över tillgänglighets zoner som betecknar den IP som tilldelats resursen måste komma från.</span><span class="sxs-lookup"><span data-stu-id="c8bbe-126">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8bbe-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c8bbe-127">-Confirm</span></span>
<span data-ttu-id="c8bbe-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c8bbe-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8bbe-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8bbe-129">-WhatIf</span></span>
<span data-ttu-id="c8bbe-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c8bbe-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8bbe-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c8bbe-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8bbe-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8bbe-132">CommonParameters</span></span>
<span data-ttu-id="c8bbe-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8bbe-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8bbe-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8bbe-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8bbe-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c8bbe-135">INPUTS</span></span>

### <span data-ttu-id="c8bbe-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c8bbe-136">System.String</span></span>

### <span data-ttu-id="c8bbe-137">System. string []</span><span class="sxs-lookup"><span data-stu-id="c8bbe-137">System.String[]</span></span>

### <span data-ttu-id="c8bbe-138">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="c8bbe-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c8bbe-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c8bbe-139">OUTPUTS</span></span>

### <span data-ttu-id="c8bbe-140">Microsoft. Azure. commands. Networks. Models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c8bbe-140">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="c8bbe-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c8bbe-141">NOTES</span></span>

## <span data-ttu-id="c8bbe-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c8bbe-142">RELATED LINKS</span></span>

[<span data-ttu-id="c8bbe-143">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c8bbe-143">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="c8bbe-144">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c8bbe-144">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="c8bbe-145">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c8bbe-145">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)