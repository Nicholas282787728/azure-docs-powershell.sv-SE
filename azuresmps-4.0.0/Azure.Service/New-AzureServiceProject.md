---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2261AD64-196A-402E-9703-EFB3A6D75FA7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d83ed3e336ca72e38fc16c27ec696eea0f84f746
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099448"
---
# <span data-ttu-id="10424-101">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="10424-101">New-AzureServiceProject</span></span>

## <span data-ttu-id="10424-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10424-102">SYNOPSIS</span></span>
<span data-ttu-id="10424-103">Skapar nödvändiga filer och konfiguration för en ny tjänst.</span><span class="sxs-lookup"><span data-stu-id="10424-103">Creates the required files and configuration for a new service.</span></span>

## <span data-ttu-id="10424-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10424-104">SYNTAX</span></span>

```
New-AzureServiceProject -ServiceName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="10424-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10424-105">DESCRIPTION</span></span>
<span data-ttu-id="10424-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="10424-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="10424-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="10424-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="10424-108">Cmdleten **New-AzureServiceProject** skapar nödvändiga filer och konfigurationer för en ny Azure-tjänst i den aktuella katalogen.</span><span class="sxs-lookup"><span data-stu-id="10424-108">The **New-AzureServiceProject** cmdlet creates the required files and configuration for a new Azure service in the current directory.</span></span>

## <span data-ttu-id="10424-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10424-109">EXAMPLES</span></span>

### <span data-ttu-id="10424-110">Exempel 1: skapa scaffolding för en tjänst</span><span class="sxs-lookup"><span data-stu-id="10424-110">Example 1: Create scaffolding for a service</span></span>
```
PS C:\> New-AzureServiceProject MyService1
```

<span data-ttu-id="10424-111">I det här exemplet skapas scaffolding för en ny Azure-tjänst som heter MyService1 i den aktuella katalogen.</span><span class="sxs-lookup"><span data-stu-id="10424-111">This example creates scaffolding for a new Azure service named MyService1 in the current directory.</span></span>

## <span data-ttu-id="10424-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10424-112">PARAMETERS</span></span>

### <span data-ttu-id="10424-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="10424-113">-Profile</span></span>
<span data-ttu-id="10424-114">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="10424-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="10424-115">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="10424-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="10424-116">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="10424-116">-ServiceName</span></span>
<span data-ttu-id="10424-117">Anger namnet på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="10424-117">Specifies the name of the service.</span></span>
<span data-ttu-id="10424-118">Den bestämmer den första delen av värd namnet för din tjänst (till exempel name.cloudapp.net) och katalogen som ska innehålla tjänsten.</span><span class="sxs-lookup"><span data-stu-id="10424-118">It determines the first section of the hostname for your service (for example, name.cloudapp.net), and the directory that will contain your service.</span></span>
<span data-ttu-id="10424-119">Namnet får bara innehålla bokstäver, siffror och bindestreck (-).</span><span class="sxs-lookup"><span data-stu-id="10424-119">The name can contain only letters, digits, and the dash character (-).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10424-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10424-120">CommonParameters</span></span>
<span data-ttu-id="10424-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10424-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10424-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10424-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10424-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10424-123">INPUTS</span></span>

## <span data-ttu-id="10424-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10424-124">OUTPUTS</span></span>

## <span data-ttu-id="10424-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10424-125">NOTES</span></span>

## <span data-ttu-id="10424-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10424-126">RELATED LINKS</span></span>

[<span data-ttu-id="10424-127">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="10424-127">Add-AzureNodeWebRole</span></span>](./Add-AzureNodeWebRole.md)

[<span data-ttu-id="10424-128">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="10424-128">Add-AzureNodeWorkerRole</span></span>](./Add-AzureNodeWorkerRole.md)

[<span data-ttu-id="10424-129">Publicera – AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="10424-129">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="10424-130">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="10424-130">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)

[<span data-ttu-id="10424-131">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="10424-131">Set-AzureServiceProjectRole</span></span>](./Set-AzureServiceProjectRole.md)


