---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
ms.openlocfilehash: 5af78bb1f915dec55f75749296340ca6d13a3b3d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525848"
---
# <span data-ttu-id="b9abc-101">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="b9abc-101">New-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="b9abc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b9abc-102">SYNOPSIS</span></span>
<span data-ttu-id="b9abc-103">Skapar en Azure-SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="b9abc-103">Creates an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="b9abc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b9abc-104">SYNTAX</span></span>

```
New-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> -Location <String>
 -SecurityProviderName <String> [-VirtualHub <PSVirtualHub>] [-VirtualHubId <String>]
 [-VirtualHubName <String>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9abc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b9abc-105">DESCRIPTION</span></span>
<span data-ttu-id="b9abc-106">Cmdleten **New-AzSecurityPartnerProvider** skapar en Azure-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="b9abc-106">The **New-AzSecurityPartnerProvider** cmdlet creates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="b9abc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b9abc-107">EXAMPLES</span></span>

### <span data-ttu-id="b9abc-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b9abc-108">Example 1</span></span>
```powershell
 New-AzSecurityPartnerProvider -Name securityPartnerProviderName -ResourceGroupName rgname -Location 'West US' -SecurityProviderName 'ZScaler'
```

## <span data-ttu-id="b9abc-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b9abc-109">PARAMETERS</span></span>

### <span data-ttu-id="b9abc-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9abc-110">-AsJob</span></span>
<span data-ttu-id="b9abc-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b9abc-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9abc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9abc-112">-DefaultProfile</span></span>
<span data-ttu-id="b9abc-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b9abc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9abc-114">-Force</span><span class="sxs-lookup"><span data-stu-id="b9abc-114">-Force</span></span>
<span data-ttu-id="b9abc-115">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="b9abc-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b9abc-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="b9abc-116">-Location</span></span>
<span data-ttu-id="b9abc-117">plats.</span><span class="sxs-lookup"><span data-stu-id="b9abc-117">location.</span></span>

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

### <span data-ttu-id="b9abc-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="b9abc-118">-Name</span></span>
<span data-ttu-id="b9abc-119">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="b9abc-119">The resource name.</span></span>

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

### <span data-ttu-id="b9abc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9abc-120">-ResourceGroupName</span></span>
<span data-ttu-id="b9abc-121">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="b9abc-121">The resource group name.</span></span>

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

### <span data-ttu-id="b9abc-122">-SecurityProviderName</span><span class="sxs-lookup"><span data-stu-id="b9abc-122">-SecurityProviderName</span></span>
<span data-ttu-id="b9abc-123">Säkerhets leverantörens namn</span><span class="sxs-lookup"><span data-stu-id="b9abc-123">The Security Provider name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ZScaler, IBoss, Checkpoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9abc-124">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b9abc-124">-Tag</span></span>
<span data-ttu-id="b9abc-125">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="b9abc-125">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b9abc-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="b9abc-126">-VirtualHub</span></span>
<span data-ttu-id="b9abc-127">ID för den virtuella hubben som säkerhets partner leverantören är kopplad till</span><span class="sxs-lookup"><span data-stu-id="b9abc-127">The virtual hub Id that the security partner provider is attached to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9abc-128">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="b9abc-128">-VirtualHubId</span></span>
<span data-ttu-id="b9abc-129">ID för VirtualHub som denna VpnGateway måste kopplas till.</span><span class="sxs-lookup"><span data-stu-id="b9abc-129">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9abc-130">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="b9abc-130">-VirtualHubName</span></span>
<span data-ttu-id="b9abc-131">ID för VirtualHub som denna VpnGateway måste kopplas till.</span><span class="sxs-lookup"><span data-stu-id="b9abc-131">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9abc-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b9abc-132">-Confirm</span></span>
<span data-ttu-id="b9abc-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b9abc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9abc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9abc-134">-WhatIf</span></span>
<span data-ttu-id="b9abc-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b9abc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9abc-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b9abc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9abc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9abc-137">CommonParameters</span></span>
<span data-ttu-id="b9abc-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9abc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9abc-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9abc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9abc-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b9abc-140">INPUTS</span></span>

### <span data-ttu-id="b9abc-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b9abc-141">System.String</span></span>

### <span data-ttu-id="b9abc-142">Microsoft. Azure. commands. Networks. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b9abc-142">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="b9abc-143">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="b9abc-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b9abc-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b9abc-144">OUTPUTS</span></span>

### <span data-ttu-id="b9abc-145">Microsoft. Azure. commands. Networks. Models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="b9abc-145">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="b9abc-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b9abc-146">NOTES</span></span>

## <span data-ttu-id="b9abc-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b9abc-147">RELATED LINKS</span></span>
