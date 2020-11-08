---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8F00099A-042A-4450-B6CF-9EDA2350CBFC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e1711bc42745b872a8e2abc8cf82e5e0e67db9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099559"
---
# <span data-ttu-id="67279-101">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="67279-101">Get-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="67279-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="67279-102">SYNOPSIS</span></span>
<span data-ttu-id="67279-103">Hämtar information om en Azure RemoteApp-samling.</span><span class="sxs-lookup"><span data-stu-id="67279-103">Retrieves information about an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="67279-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="67279-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollection [[-CollectionName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="67279-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="67279-105">DESCRIPTION</span></span>
<span data-ttu-id="67279-106">Cmdleten **Get-AzureRemoteAppCollection** hämtar information om Azure RemoteApp-samlingar i Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="67279-106">The **Get-AzureRemoteAppCollection** cmdlet retrieves information about Azure RemoteApp collections in Microsoft Azure.</span></span>
<span data-ttu-id="67279-107">Den returnerar ett objekt med information om en viss samling, eller om ingen samling anges för alla samlingar i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="67279-107">It returns an object with information on a specific collection, or if no collection is specified, for all the collections in the current subscription.</span></span>

## <span data-ttu-id="67279-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="67279-108">EXAMPLES</span></span>

### <span data-ttu-id="67279-109">Exempel 1: Visa en lista över alla samlingar</span><span class="sxs-lookup"><span data-stu-id="67279-109">Example 1: Get a list of all collections</span></span>
```
PS C:\> Get-AzureRemoteAppCollection
```

<span data-ttu-id="67279-110">Det här kommandot returnerar en lista över alla Azure RemoteApp-samlingar i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="67279-110">This command returns a list of all Azure RemoteApp collections in the subscription.</span></span>

### <span data-ttu-id="67279-111">Exempel 2: Hämta information om en viss samling</span><span class="sxs-lookup"><span data-stu-id="67279-111">Example 2: Get information about a specified collection</span></span>
```
PS C:\> Get-AzureRemoteAppCollection ContosoApps
```

<span data-ttu-id="67279-112">Det här kommandot returnerar information om Azure RemoteApp-samlingen med namnet ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="67279-112">This command returns information about the Azure RemoteApp collection named ContosoApps.</span></span>

### <span data-ttu-id="67279-113">Exempel 3: Hämta en lista med samlingar med hjälp av jokertecken</span><span class="sxs-lookup"><span data-stu-id="67279-113">Example 3: Get a list of collections by using a wildcard</span></span>
```
PS C:\> Get-AzureRemoteAppCollection Finance*
```

<span data-ttu-id="67279-114">Det här kommandot returnerar en lista över alla Azure RemoteApp-samlingar som matchar finansierings \*.</span><span class="sxs-lookup"><span data-stu-id="67279-114">This command returns a list of all Azure RemoteApp collections matching Finance\*.</span></span>

## <span data-ttu-id="67279-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="67279-115">PARAMETERS</span></span>

### <span data-ttu-id="67279-116">-Samlings namn</span><span class="sxs-lookup"><span data-stu-id="67279-116">-CollectionName</span></span>
<span data-ttu-id="67279-117">Anger namnet på Azure RemoteApp-samlingen.</span><span class="sxs-lookup"><span data-stu-id="67279-117">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="67279-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="67279-118">-Profile</span></span>
<span data-ttu-id="67279-119">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="67279-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="67279-120">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="67279-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="67279-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67279-121">CommonParameters</span></span>
<span data-ttu-id="67279-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67279-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67279-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67279-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67279-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="67279-124">INPUTS</span></span>

## <span data-ttu-id="67279-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="67279-125">OUTPUTS</span></span>

## <span data-ttu-id="67279-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="67279-126">NOTES</span></span>

## <span data-ttu-id="67279-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="67279-127">RELATED LINKS</span></span>

[<span data-ttu-id="67279-128">New-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="67279-128">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="67279-129">Remove-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="67279-129">Remove-AzureRemoteAppCollection</span></span>](./Remove-AzureRemoteAppCollection.md)

[<span data-ttu-id="67279-130">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="67279-130">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)

[<span data-ttu-id="67279-131">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="67279-131">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


