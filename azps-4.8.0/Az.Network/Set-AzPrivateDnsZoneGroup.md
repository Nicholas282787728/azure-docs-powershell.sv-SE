---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: cd9270d724e0e1523c3ee621cb58fa28a2f4bc66
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258149"
---
# <span data-ttu-id="93969-101">Set-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="93969-101">Set-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="93969-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="93969-102">SYNOPSIS</span></span>
<span data-ttu-id="93969-103">Uppdaterar DNS-zonfilen</span><span class="sxs-lookup"><span data-stu-id="93969-103">Updates DNS zone group</span></span>

## <span data-ttu-id="93969-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="93969-104">SYNTAX</span></span>

```
Set-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93969-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="93969-105">DESCRIPTION</span></span>
<span data-ttu-id="93969-106">Cmdleten **set-AzPrivateDnsZoneGroup** .</span><span class="sxs-lookup"><span data-stu-id="93969-106">The **Set-AzPrivateDnsZoneGroup** cmdlet updates DNS zone group.</span></span>

## <span data-ttu-id="93969-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="93969-107">EXAMPLES</span></span>

### <span data-ttu-id="93969-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="93969-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPrivateDnsZoneGroup -ResourceGroupName rg -PrivateEndpointName my-pr-endpoint -name dnsgroup1

Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/my-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test.vault.azure.com",
                            "RecordSets": []
                          }
                        ]

PS C:\> $zone1 = Get-AzPrivateDnsZone -ResourceGroupName rg -Name "test1.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name test1-vault-azure-com -PrivateDnsZoneId $zone1.ResourceId
PS C:\> Set-AzPrivateDnsZoneGroup -ResourceGroupName rg -PrivateEndpointName my-pr-endpoint -name dnsgroup1 -PrivateDnsZoneConfig $config -Force

Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/my-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test1-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test1.vault.azure.com",
                            "RecordSets": []
                          }
                        ]
```

<span data-ttu-id="93969-109">Ovan uppdateras exempel DNS-zonfilen med namnet dnsgroup1 med ett nytt dnsconfig som länkar till en annan DNS-zon.</span><span class="sxs-lookup"><span data-stu-id="93969-109">Above example updates DNS zone group named dnsgroup1 with a new dnsconfig which links to another DNS zone.</span></span>

## <span data-ttu-id="93969-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="93969-110">PARAMETERS</span></span>

### <span data-ttu-id="93969-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93969-111">-AsJob</span></span>
<span data-ttu-id="93969-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="93969-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="93969-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93969-113">-DefaultProfile</span></span>
<span data-ttu-id="93969-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="93969-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93969-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="93969-115">-Name</span></span>
<span data-ttu-id="93969-116">Namnet på den privata DNS-zonfilen.</span><span class="sxs-lookup"><span data-stu-id="93969-116">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="93969-117">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="93969-117">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="93969-118">En samling privata DNS-zondata för gruppen privata DNS-zoner.</span><span class="sxs-lookup"><span data-stu-id="93969-118">A collection of private dns zone configurations of the private dns zone group.</span></span>

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

### <span data-ttu-id="93969-119">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="93969-119">-PrivateEndpointName</span></span>
<span data-ttu-id="93969-120">Namnet på den privata slut punkten.</span><span class="sxs-lookup"><span data-stu-id="93969-120">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="93969-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93969-121">-ResourceGroupName</span></span>
<span data-ttu-id="93969-122">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="93969-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="93969-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="93969-123">-Confirm</span></span>
<span data-ttu-id="93969-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="93969-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93969-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93969-125">-WhatIf</span></span>
<span data-ttu-id="93969-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="93969-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93969-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="93969-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93969-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93969-128">CommonParameters</span></span>
<span data-ttu-id="93969-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93969-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93969-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93969-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93969-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="93969-131">INPUTS</span></span>

### <span data-ttu-id="93969-132">System. String</span><span class="sxs-lookup"><span data-stu-id="93969-132">System.String</span></span>

### <span data-ttu-id="93969-133">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSPrivateDnsZoneConfig, Microsoft. Azure. PowerShell. cmdletar. Network, version = 2.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="93969-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="93969-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="93969-134">OUTPUTS</span></span>

### <span data-ttu-id="93969-135">Microsoft. Azure. commands. Networks. Models. PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="93969-135">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="93969-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="93969-136">NOTES</span></span>

## <span data-ttu-id="93969-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="93969-137">RELATED LINKS</span></span>
