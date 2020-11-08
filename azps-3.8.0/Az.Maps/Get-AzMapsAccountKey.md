---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/get-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
ms.openlocfilehash: 4969ba5cdb8b24627e620b82a13806c7b4cc687e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089589"
---
# <span data-ttu-id="7835a-101">Get-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="7835a-101">Get-AzMapsAccountKey</span></span>

## <span data-ttu-id="7835a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7835a-102">SYNOPSIS</span></span>
<span data-ttu-id="7835a-103">Hämtar API-nycklarna för ett konto.</span><span class="sxs-lookup"><span data-stu-id="7835a-103">Gets the API keys for an account.</span></span>
<span data-ttu-id="7835a-104">De här nycklarna är den autentiseringsmekanism som används vid kommande samtal till Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="7835a-104">These keys are the authentication mechanism used in subsequent calls to Azure Maps.</span></span>

## <span data-ttu-id="7835a-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7835a-105">SYNTAX</span></span>

### <span data-ttu-id="7835a-106">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7835a-106">NameParameterSet (Default)</span></span>
```
Get-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7835a-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7835a-107">InputObjectParameterSet</span></span>
```
Get-AzMapsAccountKey [-InputObject <PSMapsAccount>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7835a-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7835a-108">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7835a-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7835a-109">DESCRIPTION</span></span>
<span data-ttu-id="7835a-110">Get-AzMapsAccountKey cmdlet får API-nycklarna för ett etablerat Azure Maps-konto.</span><span class="sxs-lookup"><span data-stu-id="7835a-110">The Get-AzMapsAccountKey cmdlet gets the API keys for a provisioned Azure Maps account.</span></span>
<span data-ttu-id="7835a-111">Ett Azure Maps-konto har två API-nycklar: primära och sekundära.</span><span class="sxs-lookup"><span data-stu-id="7835a-111">An Azure Maps account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="7835a-112">Nycklarna aktiverar interaktion med slut punkten för Azure Maps-kontot.</span><span class="sxs-lookup"><span data-stu-id="7835a-112">The keys enable interaction with the Azure Maps account endpoint.</span></span>
<span data-ttu-id="7835a-113">Använd New-AzMapsAccountKey (New-AzMapsAccountKey. MD) för att återskapa en ny.</span><span class="sxs-lookup"><span data-stu-id="7835a-113">Use New-AzMapsAccountKey (New-AzMapsAccountKey.md)to regenerate a key.</span></span>

## <span data-ttu-id="7835a-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7835a-114">EXAMPLES</span></span>

### <span data-ttu-id="7835a-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7835a-115">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="7835a-116">Returnerar nycklarna för kontot med namnet mitt konto i resurs gruppen MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7835a-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="7835a-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7835a-117">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="7835a-118">Returnerar nycklarna för det angivna Azure Maps-kontot.</span><span class="sxs-lookup"><span data-stu-id="7835a-118">Returns the keys for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="7835a-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7835a-119">PARAMETERS</span></span>

### <span data-ttu-id="7835a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7835a-120">-DefaultProfile</span></span>
<span data-ttu-id="7835a-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7835a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7835a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7835a-122">-InputObject</span></span>
<span data-ttu-id="7835a-123">Mappar piped från get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="7835a-123">Maps Account piped from Get-AzMapsAccount.</span></span>

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

### <span data-ttu-id="7835a-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="7835a-124">-Name</span></span>
<span data-ttu-id="7835a-125">Mappar konto namn.</span><span class="sxs-lookup"><span data-stu-id="7835a-125">Maps Account Name.</span></span>

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

### <span data-ttu-id="7835a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7835a-126">-ResourceGroupName</span></span>
<span data-ttu-id="7835a-127">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="7835a-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="7835a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7835a-128">-ResourceId</span></span>
<span data-ttu-id="7835a-129">Kopplar ihop konto-ResourceId.</span><span class="sxs-lookup"><span data-stu-id="7835a-129">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="7835a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7835a-130">CommonParameters</span></span>
<span data-ttu-id="7835a-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7835a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7835a-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7835a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7835a-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7835a-133">INPUTS</span></span>

### <span data-ttu-id="7835a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7835a-134">System.String</span></span>

### <span data-ttu-id="7835a-135">Microsoft. Azure. commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="7835a-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="7835a-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7835a-136">OUTPUTS</span></span>

### <span data-ttu-id="7835a-137">Microsoft. Azure. commands. Maps. Models. PSMapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="7835a-137">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span></span>

## <span data-ttu-id="7835a-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7835a-138">NOTES</span></span>

## <span data-ttu-id="7835a-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7835a-139">RELATED LINKS</span></span>
