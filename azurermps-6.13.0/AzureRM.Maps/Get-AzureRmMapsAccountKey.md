---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/get-azurermmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccountKey.md
ms.openlocfilehash: 1afe0f8f93bd00a384e1bb741ed8ea54e1ae66d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577936"
---
# <span data-ttu-id="983f9-101">Get-AzureRmMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="983f9-101">Get-AzureRmMapsAccountKey</span></span>

## <span data-ttu-id="983f9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="983f9-102">SYNOPSIS</span></span>
<span data-ttu-id="983f9-103">Hämtar API-nycklarna för ett konto.</span><span class="sxs-lookup"><span data-stu-id="983f9-103">Gets the API keys for an account.</span></span>
<span data-ttu-id="983f9-104">De här nycklarna är den autentiseringsmekanism som används vid kommande samtal till Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="983f9-104">These keys are the authentication mechanism used in subsequent calls to Azure Maps.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="983f9-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="983f9-105">SYNTAX</span></span>

### <span data-ttu-id="983f9-106">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="983f9-106">NameParameterSet (Default)</span></span>
```
Get-AzureRmMapsAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="983f9-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="983f9-107">InputObjectParameterSet</span></span>
```
Get-AzureRmMapsAccountKey [-InputObject <PSMapsAccount>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="983f9-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="983f9-108">ResourceIdParameterSet</span></span>
```
Get-AzureRmMapsAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="983f9-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="983f9-109">DESCRIPTION</span></span>
<span data-ttu-id="983f9-110">Get-AzureRmMapsAccountKey cmdlet får API-nycklarna för ett etablerat Azure Maps-konto.</span><span class="sxs-lookup"><span data-stu-id="983f9-110">The Get-AzureRmMapsAccountKey cmdlet gets the API keys for a provisioned Azure Maps account.</span></span>
<span data-ttu-id="983f9-111">Ett Azure Maps-konto har två API-nycklar: primära och sekundära.</span><span class="sxs-lookup"><span data-stu-id="983f9-111">An Azure Maps account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="983f9-112">Nycklarna aktiverar interaktion med slut punkten för Azure Maps-kontot.</span><span class="sxs-lookup"><span data-stu-id="983f9-112">The keys enable interaction with the Azure Maps account endpoint.</span></span>
<span data-ttu-id="983f9-113">Använd New-AzureRmMapsAccountKey (New-AzureRmMapsAccountKey. MD) för att återskapa en ny.</span><span class="sxs-lookup"><span data-stu-id="983f9-113">Use New-AzureRmMapsAccountKey (New-AzureRmMapsAccountKey.md)to regenerate a key.</span></span>

## <span data-ttu-id="983f9-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="983f9-114">EXAMPLES</span></span>

### <span data-ttu-id="983f9-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="983f9-115">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="983f9-116">Returnerar nycklarna för kontot med namnet mitt konto i resurs gruppen MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="983f9-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="983f9-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="983f9-117">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="983f9-118">Returnerar nycklarna för det angivna Azure Maps-kontot.</span><span class="sxs-lookup"><span data-stu-id="983f9-118">Returns the keys for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="983f9-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="983f9-119">PARAMETERS</span></span>

### <span data-ttu-id="983f9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="983f9-120">-DefaultProfile</span></span>
<span data-ttu-id="983f9-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="983f9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="983f9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="983f9-122">-InputObject</span></span>
<span data-ttu-id="983f9-123">Mappar piped från get-AzureRmMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="983f9-123">Maps Account piped from Get-AzureRmMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="983f9-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="983f9-124">-Name</span></span>
<span data-ttu-id="983f9-125">Mappar konto namn.</span><span class="sxs-lookup"><span data-stu-id="983f9-125">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="983f9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="983f9-126">-ResourceGroupName</span></span>
<span data-ttu-id="983f9-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="983f9-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="983f9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="983f9-128">-ResourceId</span></span>
<span data-ttu-id="983f9-129">Kopplar ihop konto-ResourceId.</span><span class="sxs-lookup"><span data-stu-id="983f9-129">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="983f9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="983f9-130">CommonParameters</span></span>
<span data-ttu-id="983f9-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="983f9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="983f9-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="983f9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="983f9-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="983f9-133">INPUTS</span></span>

### <span data-ttu-id="983f9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="983f9-134">System.String</span></span>

### <span data-ttu-id="983f9-135">Microsoft. Azure. commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="983f9-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>
<span data-ttu-id="983f9-136">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="983f9-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="983f9-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="983f9-137">OUTPUTS</span></span>

### <span data-ttu-id="983f9-138">Microsoft. Azure. commands. Maps. Models. PSMapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="983f9-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span></span>

## <span data-ttu-id="983f9-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="983f9-139">NOTES</span></span>

## <span data-ttu-id="983f9-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="983f9-140">RELATED LINKS</span></span>
