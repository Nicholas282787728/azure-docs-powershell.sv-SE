---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/get-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: 283bc1a14404c842da0ed99e43596984b1559299
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580087"
---
# <span data-ttu-id="6fbd6-101">Get-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="6fbd6-101">Get-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="6fbd6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6fbd6-102">SYNOPSIS</span></span>
<span data-ttu-id="6fbd6-103">Skaffa WAF policy</span><span class="sxs-lookup"><span data-stu-id="6fbd6-103">Get WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fbd6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6fbd6-104">SYNTAX</span></span>

```
Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fbd6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6fbd6-105">DESCRIPTION</span></span>
<span data-ttu-id="6fbd6-106">Funktionen **Get-AzureRmFrontDoorFireWallPolicy** CMDLETGET får WAF policy i en resurs grupp under den aktuella prenumerationen</span><span class="sxs-lookup"><span data-stu-id="6fbd6-106">The **Get-AzureRmFrontDoorFireWallPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="6fbd6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6fbd6-107">EXAMPLES</span></span>

### <span data-ttu-id="6fbd6-108">Exempel 1: Hämta en WAF policy som heter $Name i $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="6fbd6-108">Example 1: Get a WAF policy called $Name in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -Name $Name -ResourceGroupName $resourceGroup

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="6fbd6-109">Skaffa en WAF policy med namnet $Name i $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="6fbd6-109">Get a WAF policy called $Name in $resourceGroup</span></span>

### <span data-ttu-id="6fbd6-110">Exempel 2: Hämta alla WAF-principer i $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="6fbd6-110">Example 2: Get all WAF policy in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name1}
Name               : {Name1}
Type               :

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name2}
Name               : {Name2}
Type               :
```

<span data-ttu-id="6fbd6-111">Hämta alla WAF-principer i $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="6fbd6-111">Get all WAF policy in $resourceGroup</span></span>

## <span data-ttu-id="6fbd6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6fbd6-112">PARAMETERS</span></span>

### <span data-ttu-id="6fbd6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fbd6-113">-DefaultProfile</span></span>
<span data-ttu-id="6fbd6-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6fbd6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fbd6-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="6fbd6-115">-Name</span></span>
<span data-ttu-id="6fbd6-116">FireWallPolicy namn.</span><span class="sxs-lookup"><span data-stu-id="6fbd6-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="6fbd6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fbd6-117">-ResourceGroupName</span></span>
<span data-ttu-id="6fbd6-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="6fbd6-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fbd6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fbd6-119">CommonParameters</span></span>
<span data-ttu-id="6fbd6-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fbd6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fbd6-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fbd6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fbd6-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6fbd6-122">INPUTS</span></span>

### <span data-ttu-id="6fbd6-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6fbd6-123">System.String</span></span>

## <span data-ttu-id="6fbd6-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6fbd6-124">OUTPUTS</span></span>

### <span data-ttu-id="6fbd6-125">Microsoft. Azure. commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="6fbd6-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="6fbd6-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6fbd6-126">NOTES</span></span>

## <span data-ttu-id="6fbd6-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6fbd6-127">RELATED LINKS</span></span>

<span data-ttu-id="6fbd6-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md) 
 [Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="6fbd6-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)
[Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md)</span></span>
