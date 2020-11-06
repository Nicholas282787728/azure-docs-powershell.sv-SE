---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: d3251e0fabb99a9f16a497a445fa010a01187108
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571904"
---
# <span data-ttu-id="93c72-101">Select-AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="93c72-101">Select-AzureRmProfile</span></span>

## <span data-ttu-id="93c72-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="93c72-102">SYNOPSIS</span></span>
<span data-ttu-id="93c72-103">Läser in Azure-autentiseringsinformation från en fil.</span><span class="sxs-lookup"><span data-stu-id="93c72-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="93c72-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="93c72-104">SYNTAX</span></span>

### <span data-ttu-id="93c72-105">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="93c72-105">InMemoryProfile</span></span>
```
Select-AzureRmProfile [-Profile] <AzureRMProfile> [<CommonParameters>]
```

### <span data-ttu-id="93c72-106">ProfileFromDisk</span><span class="sxs-lookup"><span data-stu-id="93c72-106">ProfileFromDisk</span></span>
```
Select-AzureRmProfile [-Path] <String> [<CommonParameters>]
```

## <span data-ttu-id="93c72-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="93c72-107">DESCRIPTION</span></span>
<span data-ttu-id="93c72-108">Select-AzureRmProfile cmdlet läser in autentiseringsinformation från en fil för att ange Azure-miljön och-kontexten.</span><span class="sxs-lookup"><span data-stu-id="93c72-108">The Select-AzureRmProfile cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="93c72-109">Cmdlets som du kör i den aktuella sessionen använder den här informationen för att autentisera förfrågningar till Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="93c72-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="93c72-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="93c72-110">EXAMPLES</span></span>

### <span data-ttu-id="93c72-111">Exempel 1: välja en profil från en PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="93c72-111">Example 1: Selecting a profile from a PSAzureProfile</span></span>
```
PS C:\> Select-AzureRmProfile -Profile (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="93c72-112">I det här exemplet väljs en profil från ett PSAzureProfile som skickas till cmdleten.</span><span class="sxs-lookup"><span data-stu-id="93c72-112">This example selects a profile from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="93c72-113">Exempel 2: välja en profil från en JSON-fil</span><span class="sxs-lookup"><span data-stu-id="93c72-113">Example 2: Selecting a profile from a JSON file</span></span>
```
PS C:\> Select-AzureRmProfile -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="93c72-114">I det här exemplet väljs en profil från en JSON-fil som skickas till cmdleten.</span><span class="sxs-lookup"><span data-stu-id="93c72-114">This example selects a profile from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="93c72-115">Denna JSON-fil kan skapas från Save-AzureRmProfile.</span><span class="sxs-lookup"><span data-stu-id="93c72-115">This JSON file can be created from Save-AzureRmProfile.</span></span>

## <span data-ttu-id="93c72-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="93c72-116">PARAMETERS</span></span>

### <span data-ttu-id="93c72-117">-Path</span><span class="sxs-lookup"><span data-stu-id="93c72-117">-Path</span></span>
<span data-ttu-id="93c72-118">Anger sökvägen till profil information som sparats med AzureRMProfile.</span><span class="sxs-lookup"><span data-stu-id="93c72-118">Specifies the path to profile information saved by using Save-AzureRMProfile.</span></span>

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93c72-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="93c72-119">-Profile</span></span>
<span data-ttu-id="93c72-120">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="93c72-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="93c72-121">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="93c72-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureRMProfile
Parameter Sets: InMemoryProfile
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93c72-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93c72-122">CommonParameters</span></span>
<span data-ttu-id="93c72-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93c72-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93c72-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93c72-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93c72-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="93c72-125">INPUTS</span></span>

## <span data-ttu-id="93c72-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="93c72-126">OUTPUTS</span></span>

### <span data-ttu-id="93c72-127">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="93c72-127">PSAzureProfile</span></span>

## <span data-ttu-id="93c72-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="93c72-128">NOTES</span></span>

## <span data-ttu-id="93c72-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="93c72-129">RELATED LINKS</span></span>

[<span data-ttu-id="93c72-130">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="93c72-130">Get-AzureRMContext</span></span>]()

