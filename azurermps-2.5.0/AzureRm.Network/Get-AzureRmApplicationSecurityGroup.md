---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationsecuritygroup
schema: 2.0.0
ms.openlocfilehash: 52050426c34b30bcab867643fbb3e5b9c373f3f2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929041"
---
# <span data-ttu-id="0c330-101">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0c330-101">Get-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="0c330-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0c330-102">SYNOPSIS</span></span>
<span data-ttu-id="0c330-103">Hämtar en säkerhets grupp för program.</span><span class="sxs-lookup"><span data-stu-id="0c330-103">Gets an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c330-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0c330-104">SYNTAX</span></span>

```
Get-AzureRmApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c330-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0c330-105">DESCRIPTION</span></span>
<span data-ttu-id="0c330-106">Cmdleten **Get-AzureRmApplicationSecurityGroup** hämtar en säkerhets grupp för program.</span><span class="sxs-lookup"><span data-stu-id="0c330-106">The **Get-AzureRmApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="0c330-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0c330-107">EXAMPLES</span></span>

### <span data-ttu-id="0c330-108">Exempel 1: Hämta alla program säkerhets grupper.</span><span class="sxs-lookup"><span data-stu-id="0c330-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup
```

<span data-ttu-id="0c330-109">Kommandot returnerar alla program säkerhets grupper i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0c330-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="0c330-110">Exempel 2: Hämta säkerhets grupper för program i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="0c330-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="0c330-111">Kommandot returnerar alla program säkerhets grupper som tillhör resurs gruppen MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0c330-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="0c330-112">Exempel 3: Hämta en specifik program säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="0c330-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup
```

<span data-ttu-id="0c330-113">I ovanstående kommando returneras program säkerhets gruppen MyApplicationSecurityGroup under resurs gruppen MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0c330-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

## <span data-ttu-id="0c330-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0c330-114">PARAMETERS</span></span>

### <span data-ttu-id="0c330-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c330-115">-DefaultProfile</span></span>
<span data-ttu-id="0c330-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0c330-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c330-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="0c330-117">-Name</span></span>
<span data-ttu-id="0c330-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="0c330-118">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c330-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c330-119">-ResourceGroupName</span></span>
<span data-ttu-id="0c330-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="0c330-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c330-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c330-121">CommonParameters</span></span>
<span data-ttu-id="0c330-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c330-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c330-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c330-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c330-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0c330-124">INPUTS</span></span>

### <span data-ttu-id="0c330-125">System. String</span><span class="sxs-lookup"><span data-stu-id="0c330-125">System.String</span></span>

## <span data-ttu-id="0c330-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0c330-126">OUTPUTS</span></span>

### <span data-ttu-id="0c330-127">Microsoft. Azure. commands. Networks. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0c330-127">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="0c330-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0c330-128">NOTES</span></span>

## <span data-ttu-id="0c330-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0c330-129">RELATED LINKS</span></span>

[<span data-ttu-id="0c330-130">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0c330-130">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="0c330-131">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0c330-131">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="0c330-132">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0c330-132">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="0c330-133">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0c330-133">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)
