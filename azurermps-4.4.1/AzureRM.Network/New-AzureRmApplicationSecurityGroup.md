---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 97a49535ab02b2ccd75a1f7520bcd8a1e3e6264f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757274"
---
# <span data-ttu-id="b5f09-101">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b5f09-101">New-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="b5f09-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b5f09-102">SYNOPSIS</span></span>
<span data-ttu-id="b5f09-103">Skapar en säkerhets grupp för program.</span><span class="sxs-lookup"><span data-stu-id="b5f09-103">Creates an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5f09-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b5f09-104">SYNTAX</span></span>

```
New-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5f09-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b5f09-105">DESCRIPTION</span></span>
<span data-ttu-id="b5f09-106">Cmdleten **New-AzureRmApplicationSecurityGroup** skapar en säkerhets grupp för program.</span><span class="sxs-lookup"><span data-stu-id="b5f09-106">The **New-AzureRmApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="b5f09-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b5f09-107">EXAMPLES</span></span>

### <span data-ttu-id="b5f09-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b5f09-108">Example 1</span></span>
```
PS C:\> New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="b5f09-109">I det här exemplet skapas en säkerhets grupp för program utan associationer.</span><span class="sxs-lookup"><span data-stu-id="b5f09-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="b5f09-110">När det har skapats kan IP-konfigurationer i nätverks gränssnittet ingå i gruppen.</span><span class="sxs-lookup"><span data-stu-id="b5f09-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="b5f09-111">Säkerhets reglerna kan även referera till gruppen som deras källor eller destinationer.</span><span class="sxs-lookup"><span data-stu-id="b5f09-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="b5f09-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b5f09-112">PARAMETERS</span></span>

### <span data-ttu-id="b5f09-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5f09-113">-DefaultProfile</span></span>
<span data-ttu-id="b5f09-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b5f09-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5f09-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b5f09-115">-Force</span></span>
<span data-ttu-id="b5f09-116">Fråga inte efter bekräftelse om du vill skriva över en resurs.</span><span class="sxs-lookup"><span data-stu-id="b5f09-116">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="b5f09-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="b5f09-117">-Location</span></span>
<span data-ttu-id="b5f09-118">Platsen.</span><span class="sxs-lookup"><span data-stu-id="b5f09-118">The location.</span></span>

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

### <span data-ttu-id="b5f09-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="b5f09-119">-Name</span></span>
<span data-ttu-id="b5f09-120">Namnet på program säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="b5f09-120">The name of the application security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5f09-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5f09-121">-ResourceGroupName</span></span>
<span data-ttu-id="b5f09-122">Resurs grupps namnet för program säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="b5f09-122">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="b5f09-123">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b5f09-123">-Tag</span></span>
<span data-ttu-id="b5f09-124">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="b5f09-124">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5f09-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b5f09-125">-Confirm</span></span>
<span data-ttu-id="b5f09-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b5f09-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5f09-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5f09-127">-WhatIf</span></span>
<span data-ttu-id="b5f09-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b5f09-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5f09-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b5f09-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5f09-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5f09-130">CommonParameters</span></span>
<span data-ttu-id="b5f09-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5f09-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5f09-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5f09-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5f09-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b5f09-133">INPUTS</span></span>

### <span data-ttu-id="b5f09-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b5f09-134">System.String</span></span>
<span data-ttu-id="b5f09-135">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="b5f09-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b5f09-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b5f09-136">OUTPUTS</span></span>

### <span data-ttu-id="b5f09-137">Microsoft. Azure. commands. Networks. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b5f09-137">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="b5f09-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b5f09-138">NOTES</span></span>

## <span data-ttu-id="b5f09-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b5f09-139">RELATED LINKS</span></span>

[<span data-ttu-id="b5f09-140">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b5f09-140">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="b5f09-141">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b5f09-141">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="b5f09-142">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b5f09-142">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b5f09-143">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b5f09-143">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b5f09-144">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b5f09-144">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b5f09-145">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b5f09-145">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="b5f09-146">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b5f09-146">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="b5f09-147">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b5f09-147">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)
