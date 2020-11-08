---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 482E8CD6-C38F-4BD5-8214-016D0D8C7FD0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6381b8e0fac5ebf047122f131af6087d5bb5a9fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093280"
---
# <span data-ttu-id="7122b-101">Get-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="7122b-101">Get-AzureStorSimpleResource</span></span>

## <span data-ttu-id="7122b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7122b-102">SYNOPSIS</span></span>
<span data-ttu-id="7122b-103">Hämtar alla resurser som du har skapat.</span><span class="sxs-lookup"><span data-stu-id="7122b-103">Gets all resources that you created.</span></span>

## <span data-ttu-id="7122b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7122b-104">SYNTAX</span></span>

```
Get-AzureStorSimpleResource [-ResourceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7122b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7122b-105">DESCRIPTION</span></span>
<span data-ttu-id="7122b-106">Cmdleten **Get-AzureStorSimpleResource** hämtar alla resurser som du har skapat med Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="7122b-106">The **Get-AzureStorSimpleResource** cmdlet gets all resources that you created by using Azure Portal.</span></span>
<span data-ttu-id="7122b-107">Denna cmdlet hämtar information som du kan använda för att ansluta till resurserna.</span><span class="sxs-lookup"><span data-stu-id="7122b-107">The cmdlet gets details you can use to connect to the resources.</span></span>

## <span data-ttu-id="7122b-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7122b-108">EXAMPLES</span></span>

### <span data-ttu-id="7122b-109">Exempel 1: Hämta alla resurser</span><span class="sxs-lookup"><span data-stu-id="7122b-109">Example 1: Get all resources</span></span>
```
PS C:\>Get-AzureStorSimpleResource
VERBOSE: ClientRequestId: 5cd61b91-ef40-43b4-986d-156e06d2ed65_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    8838459798595306468  Started
Contoso68-Tsqa                                    2859070203638134681  Started
Contoso73-Tsqa                                    7871392677286863733  Started
Contoso87-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 4 StorSimple resources.
```

<span data-ttu-id="7122b-110">Det här kommandot får alla resurser du har skapat.</span><span class="sxs-lookup"><span data-stu-id="7122b-110">This command gets all the resources you created.</span></span>
<span data-ttu-id="7122b-111">I det här exemplet finns det tre resurser.</span><span class="sxs-lookup"><span data-stu-id="7122b-111">In this example, there are three resources.</span></span>

### <span data-ttu-id="7122b-112">Exempel 2: skaffa en resurs genom att använda dess namn</span><span class="sxs-lookup"><span data-stu-id="7122b-112">Example 2: Get a resource by using its name</span></span>
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa"
VERBOSE: ClientRequestId: efc3c85c-12aa-4345-b6eb-ccc532de4825_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 1 StorSimple resource.
```

<span data-ttu-id="7122b-113">Med det här kommandot får du resursen namnet Contoso63-Tsqa.</span><span class="sxs-lookup"><span data-stu-id="7122b-113">This command gets the resource named Contoso63-Tsqa.</span></span>

### <span data-ttu-id="7122b-114">Exempel 3: försök att hämta en resurs som inte finns</span><span class="sxs-lookup"><span data-stu-id="7122b-114">Example 3: Attempt to get a nonexistent resource</span></span>
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
VERBOSE: ClientRequestId: 5d08d40b-f9d7-4d43-956f-13f01e89625b_PS
VERBOSE: Invalid input : Could not find a resource named Contoso64-Tsqa in your subscription.
```

<span data-ttu-id="7122b-115">Det här kommandot försöker hämta resursen med namnet Contoso64-Tsqa.</span><span class="sxs-lookup"><span data-stu-id="7122b-115">This command attempts to get the resource named Contoso64-Tsqa.</span></span>
<span data-ttu-id="7122b-116">Det finns ingen resurs med det här namnet.</span><span class="sxs-lookup"><span data-stu-id="7122b-116">There is no resource that has this name.</span></span>
<span data-ttu-id="7122b-117">I det här exemplet returneras ingen resurs.</span><span class="sxs-lookup"><span data-stu-id="7122b-117">This example does not return any resource.</span></span>

## <span data-ttu-id="7122b-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7122b-118">PARAMETERS</span></span>

### <span data-ttu-id="7122b-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="7122b-119">-Profile</span></span>
<span data-ttu-id="7122b-120">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="7122b-120">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7122b-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7122b-121">-ResourceName</span></span>
<span data-ttu-id="7122b-122">Anger namnet på den resurs som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="7122b-122">Specifies the name of the resource that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7122b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7122b-123">CommonParameters</span></span>
<span data-ttu-id="7122b-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7122b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7122b-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7122b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7122b-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7122b-126">INPUTS</span></span>

### <span data-ttu-id="7122b-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="7122b-127">None</span></span>

## <span data-ttu-id="7122b-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7122b-128">OUTPUTS</span></span>

### <span data-ttu-id="7122b-129">IEnumerable \<ResourceCredentials\> , ResourceCredentials</span><span class="sxs-lookup"><span data-stu-id="7122b-129">IEnumerable\<ResourceCredentials\>, ResourceCredentials</span></span>
<span data-ttu-id="7122b-130">Denna cmdlet returnerar **ResourceCredentials** -objekt som innehåller följande egenskaper:</span><span class="sxs-lookup"><span data-stu-id="7122b-130">This cmdlet returns **ResourceCredentials** objects that contain the following properties:</span></span> 

- <span data-ttu-id="7122b-131">**ResourceName**</span><span class="sxs-lookup"><span data-stu-id="7122b-131">**ResourceName**</span></span>
- <span data-ttu-id="7122b-132">**ResouceId**</span><span class="sxs-lookup"><span data-stu-id="7122b-132">**ResouceId**</span></span>
- <span data-ttu-id="7122b-133">**ResourceState**</span><span class="sxs-lookup"><span data-stu-id="7122b-133">**ResourceState**</span></span>

## <span data-ttu-id="7122b-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7122b-134">NOTES</span></span>

## <span data-ttu-id="7122b-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7122b-135">RELATED LINKS</span></span>

[<span data-ttu-id="7122b-136">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="7122b-136">Get-AzureStorSimpleResourceContext</span></span>](./Get-AzureStorSimpleResourceContext.md)

[<span data-ttu-id="7122b-137">Select-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="7122b-137">Select-AzureStorSimpleResource</span></span>](./Select-AzureStorSimpleResource.md)


