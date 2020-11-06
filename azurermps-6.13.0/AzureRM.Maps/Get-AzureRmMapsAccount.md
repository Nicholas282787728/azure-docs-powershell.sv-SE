---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/get-azurermmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccount.md
ms.openlocfilehash: 68ccff91f6e233862ba1ee5aa94a3a3d0d8422b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584163"
---
# <span data-ttu-id="3d6c5-101">Get-AzureRmMapsAccount</span><span class="sxs-lookup"><span data-stu-id="3d6c5-101">Get-AzureRmMapsAccount</span></span>

## <span data-ttu-id="3d6c5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d6c5-102">SYNOPSIS</span></span>
<span data-ttu-id="3d6c5-103">Får kontot.</span><span class="sxs-lookup"><span data-stu-id="3d6c5-103">Gets the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d6c5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d6c5-104">SYNTAX</span></span>

### <span data-ttu-id="3d6c5-105">ResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3d6c5-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmMapsAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d6c5-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d6c5-106">AccountNameParameterSet</span></span>
```
Get-AzureRmMapsAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d6c5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d6c5-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmMapsAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d6c5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d6c5-108">DESCRIPTION</span></span>
<span data-ttu-id="3d6c5-109">Get-AzureRmMapsAccount-cmdleten får ett etablerat Azure Maps-konto, antingen via resurs grupp och-namn eller efter resurs-ID. Dessutom kan den returnera en lista över alla konton i ResourceGroup, eller alla Azure Maps-konton för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="3d6c5-109">The Get-AzureRmMapsAccount cmdlet gets a provisioned Azure Maps account, either by resource group and name, or by resource id. Additionally, it can return a list of all accounts in the ResourceGroup, or all Azure Maps accounts for the current subscription.</span></span>

## <span data-ttu-id="3d6c5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d6c5-110">EXAMPLES</span></span>

### <span data-ttu-id="3d6c5-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3d6c5-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="3d6c5-112">Hämtar kontot som heter mitt konto i resurs gruppen MyResourceGroup, om det finns.</span><span class="sxs-lookup"><span data-stu-id="3d6c5-112">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="3d6c5-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3d6c5-113">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="3d6c5-114">Hämtar alla Azure Maps-konton i resurs gruppen MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3d6c5-114">Gets all Azure Maps accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="3d6c5-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="3d6c5-115">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="3d6c5-116">Hämtar alla Azure Maps-konton i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="3d6c5-116">Gets all Azure Maps accounts in the current subscription.</span></span>

### <span data-ttu-id="3d6c5-117">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="3d6c5-117">Example 4</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="3d6c5-118">Hämtar det Maps-konto som anges av resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="3d6c5-118">Gets the Maps account specified by the Resource Id.</span></span>

## <span data-ttu-id="3d6c5-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d6c5-119">PARAMETERS</span></span>

### <span data-ttu-id="3d6c5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d6c5-120">-DefaultProfile</span></span>
<span data-ttu-id="3d6c5-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3d6c5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d6c5-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="3d6c5-122">-Name</span></span>
<span data-ttu-id="3d6c5-123">Mappar konto namn.</span><span class="sxs-lookup"><span data-stu-id="3d6c5-123">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6c5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d6c5-124">-ResourceGroupName</span></span>
<span data-ttu-id="3d6c5-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="3d6c5-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6c5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d6c5-126">-ResourceId</span></span>
<span data-ttu-id="3d6c5-127">Kopplar ihop konto-ResourceId.</span><span class="sxs-lookup"><span data-stu-id="3d6c5-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6c5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d6c5-128">CommonParameters</span></span>
<span data-ttu-id="3d6c5-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d6c5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d6c5-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d6c5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d6c5-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d6c5-131">INPUTS</span></span>

### <span data-ttu-id="3d6c5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3d6c5-132">System.String</span></span>

## <span data-ttu-id="3d6c5-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d6c5-133">OUTPUTS</span></span>

### <span data-ttu-id="3d6c5-134">Microsoft. Azure. commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="3d6c5-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="3d6c5-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d6c5-135">NOTES</span></span>

## <span data-ttu-id="3d6c5-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d6c5-136">RELATED LINKS</span></span>
