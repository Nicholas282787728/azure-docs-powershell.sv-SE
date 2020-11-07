---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationSecurityGroup.md
ms.openlocfilehash: 81eaa1f5c6e44586ae6ac9e5b6838f00063a9211
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922144"
---
# <span data-ttu-id="1d23b-101">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1d23b-101">New-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="1d23b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1d23b-102">SYNOPSIS</span></span>
<span data-ttu-id="1d23b-103">Skapar en säkerhets grupp för program.</span><span class="sxs-lookup"><span data-stu-id="1d23b-103">Creates an application security group.</span></span>

## <span data-ttu-id="1d23b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1d23b-104">SYNTAX</span></span>

```
New-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1d23b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1d23b-105">DESCRIPTION</span></span>
<span data-ttu-id="1d23b-106">Cmdleten **New-AzApplicationSecurityGroup** skapar en säkerhets grupp för program.</span><span class="sxs-lookup"><span data-stu-id="1d23b-106">The **New-AzApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="1d23b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1d23b-107">EXAMPLES</span></span>

### <span data-ttu-id="1d23b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1d23b-108">Example 1</span></span>
```
PS C:\> New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="1d23b-109">I det här exemplet skapas en säkerhets grupp för program utan associationer.</span><span class="sxs-lookup"><span data-stu-id="1d23b-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="1d23b-110">När det har skapats kan IP-konfigurationer i nätverks gränssnittet ingå i gruppen.</span><span class="sxs-lookup"><span data-stu-id="1d23b-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="1d23b-111">Säkerhets reglerna kan även referera till gruppen som deras källor eller destinationer.</span><span class="sxs-lookup"><span data-stu-id="1d23b-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="1d23b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1d23b-112">PARAMETERS</span></span>

### <span data-ttu-id="1d23b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d23b-113">-AsJob</span></span>
<span data-ttu-id="1d23b-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1d23b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d23b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d23b-115">-DefaultProfile</span></span>
<span data-ttu-id="1d23b-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1d23b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d23b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1d23b-117">-Force</span></span>
<span data-ttu-id="1d23b-118">Fråga inte efter bekräftelse om du vill skriva över en resurs.</span><span class="sxs-lookup"><span data-stu-id="1d23b-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="1d23b-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="1d23b-119">-Location</span></span>
<span data-ttu-id="1d23b-120">Platsen.</span><span class="sxs-lookup"><span data-stu-id="1d23b-120">The location.</span></span>

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

### <span data-ttu-id="1d23b-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="1d23b-121">-Name</span></span>
<span data-ttu-id="1d23b-122">Namnet på program säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="1d23b-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="1d23b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d23b-123">-ResourceGroupName</span></span>
<span data-ttu-id="1d23b-124">Resurs grupps namnet för program säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="1d23b-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="1d23b-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="1d23b-125">-Tag</span></span>
<span data-ttu-id="1d23b-126">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="1d23b-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="1d23b-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1d23b-127">-Confirm</span></span>
<span data-ttu-id="1d23b-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1d23b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d23b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d23b-129">-WhatIf</span></span>
<span data-ttu-id="1d23b-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1d23b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d23b-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1d23b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d23b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d23b-132">CommonParameters</span></span>
<span data-ttu-id="1d23b-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d23b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d23b-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d23b-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d23b-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1d23b-135">INPUTS</span></span>

### <span data-ttu-id="1d23b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1d23b-136">System.String</span></span>
<span data-ttu-id="1d23b-137">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="1d23b-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1d23b-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1d23b-138">OUTPUTS</span></span>

### <span data-ttu-id="1d23b-139">Microsoft. Azure. commands. Networks. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1d23b-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="1d23b-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1d23b-140">NOTES</span></span>

## <span data-ttu-id="1d23b-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1d23b-141">RELATED LINKS</span></span>

[<span data-ttu-id="1d23b-142">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1d23b-142">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

[<span data-ttu-id="1d23b-143">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1d23b-143">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="1d23b-144">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1d23b-144">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="1d23b-145">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1d23b-145">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="1d23b-146">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1d23b-146">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="1d23b-147">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="1d23b-147">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="1d23b-148">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="1d23b-148">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="1d23b-149">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="1d23b-149">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
