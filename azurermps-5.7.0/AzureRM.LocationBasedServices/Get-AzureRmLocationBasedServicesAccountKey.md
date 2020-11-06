---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/get-azurermlocationbasedservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccountKey.md
ms.openlocfilehash: 1f528bb0a80f039b9a2be7cb4cb6e4c7fbc740c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585120"
---
# <span data-ttu-id="51582-101">Get-AzureRmLocationBasedServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="51582-101">Get-AzureRmLocationBasedServicesAccountKey</span></span>

## <span data-ttu-id="51582-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51582-102">SYNOPSIS</span></span>
<span data-ttu-id="51582-103">Hämtar API-nycklarna för ett konto.</span><span class="sxs-lookup"><span data-stu-id="51582-103">Gets the API keys for an account.</span></span> <span data-ttu-id="51582-104">De här nycklarna är den autentiseringsmekanism som används vid efterföljande samtal till Azure location-baserade tjänster.</span><span class="sxs-lookup"><span data-stu-id="51582-104">These keys are the authentication mechanism used in subsequent calls to Azure Location Based Services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51582-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51582-105">SYNTAX</span></span>

### <span data-ttu-id="51582-106">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="51582-106">NameParameterSet (Default)</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51582-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51582-107">InputObjectParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-InputObject <PSLocationBasedServicesAccount>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51582-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51582-108">ResourceIdParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="51582-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51582-109">DESCRIPTION</span></span>
<span data-ttu-id="51582-110">Cmdleten **Get-AzureRmLocationBasedServicesAccountKey** hämtar API-nycklarna för ett etablerat tjänst konto.</span><span class="sxs-lookup"><span data-stu-id="51582-110">The **Get-AzureRmLocationBasedServicesAccountKey** cmdlet gets the API keys for a provisioned Location Based Services account.</span></span>

<span data-ttu-id="51582-111">Ett konto för platsbaserade tjänster har två API-nycklar: primära och sekundära.</span><span class="sxs-lookup"><span data-stu-id="51582-111">A Location Based Services account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="51582-112">Med tangenterna kan du använda slut punkten för det platsbaserade tjänste kontot.</span><span class="sxs-lookup"><span data-stu-id="51582-112">The keys enable interaction with the Location Based Services account endpoint.</span></span>

<span data-ttu-id="51582-113">Använd [New-AzureRmLocationBasedServicesAccountKey](New-AzureRmLocationBasedServicesAccountKey.md) för att återskapa en ny.</span><span class="sxs-lookup"><span data-stu-id="51582-113">Use [New-AzureRmLocationBasedServicesAccountKey](New-AzureRmLocationBasedServicesAccountKey.md) to regenerate a key.</span></span>

## <span data-ttu-id="51582-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51582-114">EXAMPLES</span></span>

### <span data-ttu-id="51582-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="51582-115">Example 1</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="51582-116">Returnerar nycklarna för kontot med namnet mitt konto i resurs gruppen MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="51582-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="51582-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="51582-117">Example 2</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="51582-118">Returnerar nycklarna för det angivna platsbaserade tjänst kontot.</span><span class="sxs-lookup"><span data-stu-id="51582-118">Returns the keys for the specified Location Based Services Account.</span></span>

## <span data-ttu-id="51582-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51582-119">PARAMETERS</span></span>

### <span data-ttu-id="51582-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51582-120">-DefaultProfile</span></span>
<span data-ttu-id="51582-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="51582-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51582-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51582-122">-InputObject</span></span>
<span data-ttu-id="51582-123">Piped från [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span><span class="sxs-lookup"><span data-stu-id="51582-123">Location Based Services Account piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span></span>

```yaml
Type: PSLocationBasedServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51582-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="51582-124">-Name</span></span>
<span data-ttu-id="51582-125">Konto namn för platsbaserade tjänster.</span><span class="sxs-lookup"><span data-stu-id="51582-125">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51582-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51582-126">-ResourceGroupName</span></span>
<span data-ttu-id="51582-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="51582-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51582-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51582-128">-ResourceId</span></span>
<span data-ttu-id="51582-129">Platsbaserade tjänst konton ResourceId.</span><span class="sxs-lookup"><span data-stu-id="51582-129">Location Based Services Account ResourceId.</span></span>
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

### <span data-ttu-id="51582-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51582-130">CommonParameters</span></span>
<span data-ttu-id="51582-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51582-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51582-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51582-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51582-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51582-133">INPUTS</span></span>

### <span data-ttu-id="51582-134">System. String</span><span class="sxs-lookup"><span data-stu-id="51582-134">System.String</span></span>

## <span data-ttu-id="51582-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51582-135">OUTPUTS</span></span>

### <span data-ttu-id="51582-136">Microsoft. Azure. commands. LocationBasedServices. Models. PSLocationBasedServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="51582-136">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccountKeys</span></span>

### <span data-ttu-id="51582-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51582-137">CommonParameters</span></span>
<span data-ttu-id="51582-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51582-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51582-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51582-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51582-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51582-140">NOTES</span></span>

## <span data-ttu-id="51582-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51582-141">RELATED LINKS</span></span>
