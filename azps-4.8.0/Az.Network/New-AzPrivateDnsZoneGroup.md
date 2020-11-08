---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: fff326143cf2740a085a6fcc3daa5dc89cdee646
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102691"
---
# <span data-ttu-id="83b2b-101">New-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="83b2b-101">New-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="83b2b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="83b2b-102">SYNOPSIS</span></span>
<span data-ttu-id="83b2b-103">Skapar en privat DNS-zonfil i den angivna privata slut punkten.</span><span class="sxs-lookup"><span data-stu-id="83b2b-103">Creates a private DNS zone group in the specified private endpoint.</span></span>

## <span data-ttu-id="83b2b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="83b2b-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83b2b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="83b2b-105">DESCRIPTION</span></span>
<span data-ttu-id="83b2b-106">Med **New-AzPrivateDnsZoneGroup** cmdlet kan du skapa en ny privat DNS-zonfil.</span><span class="sxs-lookup"><span data-stu-id="83b2b-106">The **New-AzPrivateDnsZoneGroup** cmdlet enables you to create a new private DNS zone group.</span></span>

## <span data-ttu-id="83b2b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="83b2b-107">EXAMPLES</span></span>

### <span data-ttu-id="83b2b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="83b2b-108">Example 1</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
PS C:\> New-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name "dnsgroup1" -PrivateDnsZoneConfig $config -Force
Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/test-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test.vault.azure.com",
                            "RecordSets": []
                          }
                        ]
```

<span data-ttu-id="83b2b-109">När privat slut punkt skapas skapas en `test-pr-endpoint` DNS-zonfil i exemplet ovan under den privata slut punkten.</span><span class="sxs-lookup"><span data-stu-id="83b2b-109">Once private endpoint `test-pr-endpoint` is created, above example creates DNS zone group under that private endpoint.</span></span>

## <span data-ttu-id="83b2b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="83b2b-110">PARAMETERS</span></span>

### <span data-ttu-id="83b2b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="83b2b-111">-AsJob</span></span>
<span data-ttu-id="83b2b-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="83b2b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="83b2b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83b2b-113">-DefaultProfile</span></span>
<span data-ttu-id="83b2b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="83b2b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83b2b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="83b2b-115">-Force</span></span>
<span data-ttu-id="83b2b-116">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="83b2b-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="83b2b-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="83b2b-117">-Name</span></span>
<span data-ttu-id="83b2b-118">Namnet på den privata DNS-zonfilen.</span><span class="sxs-lookup"><span data-stu-id="83b2b-118">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="83b2b-119">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="83b2b-119">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="83b2b-120">En samling privata DNS-zondata för gruppen privata DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="83b2b-120">A collection of private dns zone configurations of the private dns zone group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83b2b-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="83b2b-121">-PrivateEndpointName</span></span>
<span data-ttu-id="83b2b-122">Namnet på den privata slut punkten.</span><span class="sxs-lookup"><span data-stu-id="83b2b-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="83b2b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83b2b-123">-ResourceGroupName</span></span>
<span data-ttu-id="83b2b-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="83b2b-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="83b2b-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="83b2b-125">-Confirm</span></span>
<span data-ttu-id="83b2b-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="83b2b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83b2b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83b2b-127">-WhatIf</span></span>
<span data-ttu-id="83b2b-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="83b2b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83b2b-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="83b2b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83b2b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83b2b-130">CommonParameters</span></span>
<span data-ttu-id="83b2b-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83b2b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83b2b-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83b2b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83b2b-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="83b2b-133">INPUTS</span></span>

### <span data-ttu-id="83b2b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="83b2b-134">System.String</span></span>

### <span data-ttu-id="83b2b-135">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSPrivateDnsZoneConfig, Microsoft. Azure. PowerShell. cmdletar. Network, version = 2.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="83b2b-135">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="83b2b-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="83b2b-136">OUTPUTS</span></span>

### <span data-ttu-id="83b2b-137">Microsoft. Azure. commands. Networks. Models. PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="83b2b-137">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="83b2b-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="83b2b-138">NOTES</span></span>

## <span data-ttu-id="83b2b-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="83b2b-139">RELATED LINKS</span></span>
