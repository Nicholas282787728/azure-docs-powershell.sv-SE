---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/get-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 18f492147e897b8061795434c309cc63729bec5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575630"
---
# <span data-ttu-id="7e639-101">Get-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7e639-101">Get-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="7e639-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7e639-102">SYNOPSIS</span></span>
<span data-ttu-id="7e639-103">Får kontot.</span><span class="sxs-lookup"><span data-stu-id="7e639-103">Gets the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e639-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7e639-104">SYNTAX</span></span>

### <span data-ttu-id="7e639-105">ResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7e639-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmLocationBasedServicesAccount [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e639-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e639-106">AccountNameParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e639-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e639-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e639-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7e639-108">DESCRIPTION</span></span>
<span data-ttu-id="7e639-109">Cmdleten **Get-AzureRmLocationBasedServicesAccount** får ett konto för etablerade tjänstbaserade tjänster, antingen via resurs grupp och-namn eller efter resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="7e639-109">The **Get-AzureRmLocationBasedServicesAccount** cmdlet gets a provisioned Location Based Services account, either by resource group and name, or by resource id.</span></span>

<span data-ttu-id="7e639-110">Dessutom kan den returnera en lista över alla konton i ResourceGroup, eller alla tjänst konton för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="7e639-110">Additionally, it can return a list of all accounts in the ResourceGroup, or all Location Based Services accounts for the current subscription.</span></span>

## <span data-ttu-id="7e639-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7e639-111">EXAMPLES</span></span>

### <span data-ttu-id="7e639-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7e639-112">Example 1</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="7e639-113">Hämtar kontot som heter mitt konto i resurs gruppen MyResourceGroup, om det finns.</span><span class="sxs-lookup"><span data-stu-id="7e639-113">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="7e639-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7e639-114">Example 2</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
[...]
```

<span data-ttu-id="7e639-115">Hämtar alla platsbaserade tjänst konton i resurs gruppen MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7e639-115">Gets all Location Based Services accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="7e639-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="7e639-116">Example 3</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
[...]
```

<span data-ttu-id="7e639-117">Hämtar alla platsbaserade tjänst konton i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="7e639-117">Gets all Location Based Services accounts in the current subscription.</span></span>

### <span data-ttu-id="7e639-118">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="7e639-118">Example 4</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="7e639-119">Hämtar det platsbaserade tjänst kontot som anges av resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="7e639-119">Gets the Location Based Services account specified by the Resource Id.</span></span>

## <span data-ttu-id="7e639-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7e639-120">PARAMETERS</span></span>

### <span data-ttu-id="7e639-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e639-121">-DefaultProfile</span></span>
<span data-ttu-id="7e639-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7e639-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e639-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="7e639-123">-Name</span></span>
<span data-ttu-id="7e639-124">Konto namn för platsbaserade tjänster.</span><span class="sxs-lookup"><span data-stu-id="7e639-124">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e639-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e639-125">-ResourceGroupName</span></span>
<span data-ttu-id="7e639-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="7e639-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e639-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e639-127">-ResourceId</span></span>
<span data-ttu-id="7e639-128">Platsbaserade tjänst konton ResourceId.</span><span class="sxs-lookup"><span data-stu-id="7e639-128">Location Based Services Account ResourceId.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e639-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e639-129">CommonParameters</span></span>
<span data-ttu-id="7e639-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e639-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e639-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e639-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e639-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7e639-132">INPUTS</span></span>

### <span data-ttu-id="7e639-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7e639-133">System.String</span></span>

## <span data-ttu-id="7e639-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7e639-134">OUTPUTS</span></span>

### <span data-ttu-id="7e639-135">Microsoft. Azure. commands. LocationBasedServices. Models. PSLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7e639-135">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccount</span></span>
<span data-ttu-id="7e639-136">Denna cmdlet returnerar ett **PSLocationBasedServicesAccount** -objekt.</span><span class="sxs-lookup"><span data-stu-id="7e639-136">This cmdlet returns a **PSLocationBasedServicesAccount** object.</span></span>
<span data-ttu-id="7e639-137">Du kan ändra det här objektet och sedan tillämpa ändringar med hjälp av **set-AzureRmLocationBasedServices**.</span><span class="sxs-lookup"><span data-stu-id="7e639-137">You can modify this object, and then apply changes by using **Set-AzureRmLocationBasedServices**.</span></span>

## <span data-ttu-id="7e639-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7e639-138">NOTES</span></span>

## <span data-ttu-id="7e639-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7e639-139">RELATED LINKS</span></span>
