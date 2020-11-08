---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7CB42968-8F6F-4D84-9AE2-1000F280BF3C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 586abbd5f203ce00f6faa7975d9e2adbd0c7940e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099779"
---
# <span data-ttu-id="0ab03-101">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="0ab03-101">Get-AzureStorSimpleResourceContext</span></span>

## <span data-ttu-id="0ab03-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0ab03-102">SYNOPSIS</span></span>
<span data-ttu-id="0ab03-103">Hämtar den aktuella resurs kontexten.</span><span class="sxs-lookup"><span data-stu-id="0ab03-103">Gets the current resource context.</span></span>

## <span data-ttu-id="0ab03-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0ab03-104">SYNTAX</span></span>

```
Get-AzureStorSimpleResourceContext [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0ab03-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0ab03-105">DESCRIPTION</span></span>
<span data-ttu-id="0ab03-106">Cmdleten **Get-AzureStorSimpleResourceContext** hämtar den aktuella resurs kontexten.</span><span class="sxs-lookup"><span data-stu-id="0ab03-106">The **Get-AzureStorSimpleResourceContext** cmdlet gets the current resource context.</span></span>

## <span data-ttu-id="0ab03-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0ab03-107">EXAMPLES</span></span>

### <span data-ttu-id="0ab03-108">Exempel 1: hämta den aktuella kontexten</span><span class="sxs-lookup"><span data-stu-id="0ab03-108">Example 1: Get the current context</span></span>
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa" 
PS C:\> Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso63-Tsqa
```

<span data-ttu-id="0ab03-109">Det första kommandot ställer in den aktuella kontexten så att den blir resursen som heter Contoso63-Tsqa genom att använda cmdleten **Select-AzureStorSimpleResource** .</span><span class="sxs-lookup"><span data-stu-id="0ab03-109">The first command sets the current context to be the resource named Contoso63-Tsqa by using the **Select-AzureStorSimpleResource** cmdlet.</span></span>

<span data-ttu-id="0ab03-110">Det andra kommandot får den aktuella resurs kontexten.</span><span class="sxs-lookup"><span data-stu-id="0ab03-110">The second command gets the current resource context.</span></span>

### <span data-ttu-id="0ab03-111">Exempel 2: försök att hämta den aktuella kontexten</span><span class="sxs-lookup"><span data-stu-id="0ab03-111">Example 2: Attempt to get the current context</span></span>
```
PS C:\>Get-AzureStorSimpleResourceContext
Get-AzureStorSimpleResourceContext : Resource Context is not set for your subscription. Please use
Select-AzureStorSimpleResource -ResourceName <<name>> to set
```

<span data-ttu-id="0ab03-112">Det här kommandot får den aktuella kontexten.</span><span class="sxs-lookup"><span data-stu-id="0ab03-112">This command gets the current context.</span></span>
<span data-ttu-id="0ab03-113">I det här exemplet har ingen kontext ställts in.</span><span class="sxs-lookup"><span data-stu-id="0ab03-113">In this example, no context has been set.</span></span>
<span data-ttu-id="0ab03-114">Kommandot returnerar ett meddelande som förklarar problemet.</span><span class="sxs-lookup"><span data-stu-id="0ab03-114">The command returns a message that explains the problem.</span></span>

## <span data-ttu-id="0ab03-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0ab03-115">PARAMETERS</span></span>

### <span data-ttu-id="0ab03-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="0ab03-116">-Profile</span></span>
<span data-ttu-id="0ab03-117">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="0ab03-117">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="0ab03-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ab03-118">CommonParameters</span></span>
<span data-ttu-id="0ab03-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ab03-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ab03-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ab03-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ab03-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0ab03-121">INPUTS</span></span>

### <span data-ttu-id="0ab03-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="0ab03-122">None</span></span>

## <span data-ttu-id="0ab03-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0ab03-123">OUTPUTS</span></span>

### <span data-ttu-id="0ab03-124">StorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="0ab03-124">StorSimpleResourceContext</span></span>
<span data-ttu-id="0ab03-125">Denna cmdlet returnerar ett **ResourceContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="0ab03-125">This cmdlet returns a **ResourceContext** object.</span></span>

## <span data-ttu-id="0ab03-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0ab03-126">NOTES</span></span>

## <span data-ttu-id="0ab03-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0ab03-127">RELATED LINKS</span></span>

[<span data-ttu-id="0ab03-128">Get-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="0ab03-128">Get-AzureStorSimpleResource</span></span>](./Get-AzureStorSimpleResource.md)

[<span data-ttu-id="0ab03-129">Select-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="0ab03-129">Select-AzureStorSimpleResource</span></span>](./Select-AzureStorSimpleResource.md)


