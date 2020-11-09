---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: 1012bd4da163b992aec049643feb1e3fd8b4bf76
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325812"
---
# <span data-ttu-id="978cf-101">Remove-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="978cf-101">Remove-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="978cf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="978cf-102">SYNOPSIS</span></span>
<span data-ttu-id="978cf-103">Tar bort en DNS-zonfil.</span><span class="sxs-lookup"><span data-stu-id="978cf-103">Removes a DNS zone group.</span></span>

## <span data-ttu-id="978cf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="978cf-104">SYNTAX</span></span>

```
Remove-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="978cf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="978cf-105">DESCRIPTION</span></span>
<span data-ttu-id="978cf-106">Cmdleten **Remove-AzPrivateDnsZoneGroup** tar bort en DNS-zonfil.</span><span class="sxs-lookup"><span data-stu-id="978cf-106">The **Remove-AzPrivateDnsZoneGroup** cmdlet removes a DNS zone group.</span></span> 

## <span data-ttu-id="978cf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="978cf-107">EXAMPLES</span></span>

### <span data-ttu-id="978cf-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="978cf-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name dnsgroup1 
```

<span data-ttu-id="978cf-109">Ovan exemplet tar bort en DNS-zon grup med namnet dnsgroup1 from slut punkts test-PR-slut punkt.</span><span class="sxs-lookup"><span data-stu-id="978cf-109">Above example removes a DNS zone grup named dnsgroup1 from endpoint test-pr-endpoint.</span></span>

## <span data-ttu-id="978cf-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="978cf-110">PARAMETERS</span></span>

### <span data-ttu-id="978cf-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="978cf-111">-AsJob</span></span>
<span data-ttu-id="978cf-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="978cf-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="978cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="978cf-113">-DefaultProfile</span></span>
<span data-ttu-id="978cf-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="978cf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="978cf-115">-Force</span><span class="sxs-lookup"><span data-stu-id="978cf-115">-Force</span></span>
<span data-ttu-id="978cf-116">Fråga inte efter bekräftelse om du vill ta bort resursen</span><span class="sxs-lookup"><span data-stu-id="978cf-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="978cf-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="978cf-117">-Name</span></span>
<span data-ttu-id="978cf-118">Namnet på den privata DNS-zonfilen.</span><span class="sxs-lookup"><span data-stu-id="978cf-118">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="978cf-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="978cf-119">-PassThru</span></span>
<span data-ttu-id="978cf-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="978cf-120">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="978cf-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="978cf-121">-PrivateEndpointName</span></span>
<span data-ttu-id="978cf-122">Namnet på den privata slut punkten.</span><span class="sxs-lookup"><span data-stu-id="978cf-122">The name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="978cf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="978cf-123">-ResourceGroupName</span></span>
<span data-ttu-id="978cf-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="978cf-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="978cf-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="978cf-125">-Confirm</span></span>
<span data-ttu-id="978cf-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="978cf-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="978cf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="978cf-127">-WhatIf</span></span>
<span data-ttu-id="978cf-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="978cf-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="978cf-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="978cf-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="978cf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="978cf-130">CommonParameters</span></span>
<span data-ttu-id="978cf-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="978cf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="978cf-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="978cf-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="978cf-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="978cf-133">INPUTS</span></span>

### <span data-ttu-id="978cf-134">System. String</span><span class="sxs-lookup"><span data-stu-id="978cf-134">System.String</span></span>

## <span data-ttu-id="978cf-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="978cf-135">OUTPUTS</span></span>

### <span data-ttu-id="978cf-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="978cf-136">System.Boolean</span></span>

## <span data-ttu-id="978cf-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="978cf-137">NOTES</span></span>

## <span data-ttu-id="978cf-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="978cf-138">RELATED LINKS</span></span>
