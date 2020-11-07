---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationsecuritygroup
schema: 2.0.0
ms.openlocfilehash: 99c863861bdf6a434e1268dcb1d9dd55ff8d9f80
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928997"
---
# <span data-ttu-id="5f6d7-101">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5f6d7-101">New-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="5f6d7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f6d7-102">SYNOPSIS</span></span>
<span data-ttu-id="5f6d7-103">Skapar en säkerhets grupp för program.</span><span class="sxs-lookup"><span data-stu-id="5f6d7-103">Creates an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f6d7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f6d7-104">SYNTAX</span></span>

```
New-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5f6d7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f6d7-105">DESCRIPTION</span></span>
<span data-ttu-id="5f6d7-106">Cmdleten **New-AzureRmApplicationSecurityGroup** skapar en säkerhets grupp för program.</span><span class="sxs-lookup"><span data-stu-id="5f6d7-106">The **New-AzureRmApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="5f6d7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f6d7-107">EXAMPLES</span></span>

### <span data-ttu-id="5f6d7-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5f6d7-108">Example 1</span></span>
```
PS C:\> New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="5f6d7-109">I det här exemplet skapas en säkerhets grupp för program utan associationer.</span><span class="sxs-lookup"><span data-stu-id="5f6d7-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="5f6d7-110">När det har skapats kan IP-konfigurationer i nätverks gränssnittet ingå i gruppen.</span><span class="sxs-lookup"><span data-stu-id="5f6d7-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="5f6d7-111">Säkerhets reglerna kan även referera till gruppen som deras källor eller destinationer.</span><span class="sxs-lookup"><span data-stu-id="5f6d7-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="5f6d7-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f6d7-112">PARAMETERS</span></span>

### <span data-ttu-id="5f6d7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5f6d7-113">-AsJob</span></span>
<span data-ttu-id="5f6d7-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="5f6d7-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5f6d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f6d7-115">-DefaultProfile</span></span>
<span data-ttu-id="5f6d7-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5f6d7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f6d7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5f6d7-117">-Force</span></span>
<span data-ttu-id="5f6d7-118">Fråga inte efter bekräftelse om du vill skriva över en resurs.</span><span class="sxs-lookup"><span data-stu-id="5f6d7-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="5f6d7-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="5f6d7-119">-Location</span></span>
<span data-ttu-id="5f6d7-120">Platsen.</span><span class="sxs-lookup"><span data-stu-id="5f6d7-120">The location.</span></span>

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

### <span data-ttu-id="5f6d7-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="5f6d7-121">-Name</span></span>
<span data-ttu-id="5f6d7-122">Namnet på program säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="5f6d7-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="5f6d7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f6d7-123">-ResourceGroupName</span></span>
<span data-ttu-id="5f6d7-124">Resurs grupps namnet för program säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="5f6d7-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="5f6d7-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="5f6d7-125">-Tag</span></span>
<span data-ttu-id="5f6d7-126">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="5f6d7-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="5f6d7-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5f6d7-127">-Confirm</span></span>
<span data-ttu-id="5f6d7-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5f6d7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f6d7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f6d7-129">-WhatIf</span></span>
<span data-ttu-id="5f6d7-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5f6d7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f6d7-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5f6d7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f6d7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f6d7-132">CommonParameters</span></span>
<span data-ttu-id="5f6d7-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f6d7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f6d7-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f6d7-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f6d7-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f6d7-135">INPUTS</span></span>

### <span data-ttu-id="5f6d7-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5f6d7-136">System.String</span></span>
<span data-ttu-id="5f6d7-137">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="5f6d7-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5f6d7-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f6d7-138">OUTPUTS</span></span>

### <span data-ttu-id="5f6d7-139">Microsoft. Azure. commands. Networks. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5f6d7-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="5f6d7-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f6d7-140">NOTES</span></span>

## <span data-ttu-id="5f6d7-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f6d7-141">RELATED LINKS</span></span>

[<span data-ttu-id="5f6d7-142">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5f6d7-142">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="5f6d7-143">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5f6d7-143">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="5f6d7-144">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5f6d7-144">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="5f6d7-145">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5f6d7-145">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="5f6d7-146">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5f6d7-146">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="5f6d7-147">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="5f6d7-147">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="5f6d7-148">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="5f6d7-148">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="5f6d7-149">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="5f6d7-149">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)
