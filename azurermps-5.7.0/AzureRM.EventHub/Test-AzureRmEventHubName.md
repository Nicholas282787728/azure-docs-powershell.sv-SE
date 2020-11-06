---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/test-azurermeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
ms.openlocfilehash: e1b6de255896adbf8fd47eb57973b5c5df0d79a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576523"
---
# <span data-ttu-id="b6cbb-101">Test-AzureRmEventHubName</span><span class="sxs-lookup"><span data-stu-id="b6cbb-101">Test-AzureRmEventHubName</span></span>

## <span data-ttu-id="b6cbb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b6cbb-102">SYNOPSIS</span></span>
<span data-ttu-id="b6cbb-103">Kontrollerar tillgänglighet för det angivna namn området eller aliaset (DR-konfigurationsfilen)</span><span class="sxs-lookup"><span data-stu-id="b6cbb-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6cbb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b6cbb-104">SYNTAX</span></span>

### <span data-ttu-id="b6cbb-105">NamespaceCheckNameAvailabilitySet (standard)</span><span class="sxs-lookup"><span data-stu-id="b6cbb-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzureRmEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6cbb-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b6cbb-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzureRmEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6cbb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b6cbb-107">DESCRIPTION</span></span>
<span data-ttu-id="b6cbb-108">**Test-AzureRmEventhubName** cmdlet kontrollerar tillgänglighet för namn områdes namnet eller aliaset (Dr-konfigurationsfilen)</span><span class="sxs-lookup"><span data-stu-id="b6cbb-108">The **Test-AzureRmEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="b6cbb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b6cbb-109">EXAMPLES</span></span>

### <span data-ttu-id="b6cbb-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b6cbb-110">Example 1</span></span>
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="b6cbb-111">Returnerar statusen för tillgänglighet för namn områdes namnet "MyNameSapceName" som sant</span><span class="sxs-lookup"><span data-stu-id="b6cbb-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="b6cbb-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b6cbb-112">Example 2</span></span>
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="b6cbb-113">Returnerar status för tillgänglighet för namn områdes namnet "MyNameSapceName" som falskt med anledning</span><span class="sxs-lookup"><span data-stu-id="b6cbb-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="b6cbb-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="b6cbb-114">Example 3</span></span>
```
PS C:\> Test-AzureRmEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="b6cbb-115">Returnerar statusen för tillgänglighet för aliasnamnet ' myAliasName ' under namn område ' MyNameSapceName ' som sant</span><span class="sxs-lookup"><span data-stu-id="b6cbb-115">Returns the status on availability of the alias name 'myAliasName' under namespace 'MyNameSapceName' as True</span></span>

## <span data-ttu-id="b6cbb-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b6cbb-116">PARAMETERS</span></span>

### <span data-ttu-id="b6cbb-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="b6cbb-117">-AliasName</span></span>
<span data-ttu-id="b6cbb-118">Namn på DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="b6cbb-118">DR Configuration Name - Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6cbb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6cbb-119">-DefaultProfile</span></span>
<span data-ttu-id="b6cbb-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b6cbb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6cbb-121">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="b6cbb-121">-Namespace</span></span>
<span data-ttu-id="b6cbb-122">Namn område för Eventhub</span><span class="sxs-lookup"><span data-stu-id="b6cbb-122">Eventhub Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6cbb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6cbb-123">-ResourceGroupName</span></span>
<span data-ttu-id="b6cbb-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="b6cbb-124">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6cbb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6cbb-125">CommonParameters</span></span>
<span data-ttu-id="b6cbb-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6cbb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b6cbb-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6cbb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6cbb-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b6cbb-128">INPUTS</span></span>

### <span data-ttu-id="b6cbb-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b6cbb-129">System.String</span></span>


## <span data-ttu-id="b6cbb-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b6cbb-130">OUTPUTS</span></span>

### <span data-ttu-id="b6cbb-131">Microsoft. Azure. commands. EventHub. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="b6cbb-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>


## <span data-ttu-id="b6cbb-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b6cbb-132">NOTES</span></span>

## <span data-ttu-id="b6cbb-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b6cbb-133">RELATED LINKS</span></span>
