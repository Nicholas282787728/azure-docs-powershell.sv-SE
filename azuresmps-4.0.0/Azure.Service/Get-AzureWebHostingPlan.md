---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3B3F1870-348D-4303-9520-FD81D4650F5F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2103a155b12fdf1e481173d529ff3308a3b2200b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099742"
---
# <span data-ttu-id="7784b-101">Get-AzureWebHostingPlan</span><span class="sxs-lookup"><span data-stu-id="7784b-101">Get-AzureWebHostingPlan</span></span>

## <span data-ttu-id="7784b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7784b-102">SYNOPSIS</span></span>
<span data-ttu-id="7784b-103">Hämtar Azure Web Hosting-abonnemang i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="7784b-103">Gets Azure web hosting plans in the current subscription.</span></span>

## <span data-ttu-id="7784b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7784b-104">SYNTAX</span></span>

```
Get-AzureWebHostingPlan [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="7784b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7784b-105">DESCRIPTION</span></span>
<span data-ttu-id="7784b-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="7784b-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7784b-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="7784b-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7784b-108">Cmdleten **Get-AzureWebHostingPlan** får Azure Web Hosting-abonnemangen i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="7784b-108">The **Get-AzureWebHostingPlan** cmdlet gets the Azure web hosting plans in the current subscription.</span></span>

<span data-ttu-id="7784b-109">Som standard får **Get-AzureWebHostingPlan** alla Azure hosting-abonnemang i det aktuella abonnemanget och returnerar ett objekt med grundläggande information om abonnemangen.</span><span class="sxs-lookup"><span data-stu-id="7784b-109">By default, **Get-AzureWebHostingPlan** gets all Azure hosting plans in the current subscription and returns an object that provides basic information about the plans.</span></span>
<span data-ttu-id="7784b-110">När du använder parametrarna *webspace* och *Name* returnerar **-AzureWebHostingPlan** ett specifikt värd Plans objekt.</span><span class="sxs-lookup"><span data-stu-id="7784b-110">When you use the *WebSpace* and *Name* parameters, **Get-AzureWebHostingPlan** returns a specific hosting plan object.</span></span>

<span data-ttu-id="7784b-111">Använd den *aktuella* parametern för cmdleten **Get-AzureSubscription** för att hitta den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="7784b-111">To find the current subscription, use the *Current* parameter of the **Get-AzureSubscription** cmdlet.</span></span>
<span data-ttu-id="7784b-112">Använd cmdleten **Select-AzureSubscription** för att ändra aktuell prenumeration.</span><span class="sxs-lookup"><span data-stu-id="7784b-112">To change the current subscription, use the **Select-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="7784b-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7784b-113">EXAMPLES</span></span>

### <span data-ttu-id="7784b-114">Exempel 1: skaffa alla webbhotell i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="7784b-114">Example 1: Get all web hosting plans in a subscription</span></span>
```
PS C:\> Get-AzureWebHostingPlan 

Name : Default1 
SKU : Basic 
WorkerSize : Small 
NumberOfWorkers : 1 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 1 
Status : Ready 
WebSpace : eastuswebspace 
Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready
```

<span data-ttu-id="7784b-115">Det här kommandot får alla Azure Web Hosting-abonnemang i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="7784b-115">This command gets all Azure web hosting plans in the current subscription.</span></span>

### <span data-ttu-id="7784b-116">Exempel 2: skaffa ett visst webb värd abonnemang i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="7784b-116">Example 2: Get a specific web hosting plan in a subscription</span></span>
```
PS C:\> Get-AzureWebHostingPlan -WebSpaceName "westeuropewebspace" -Name "Default0" 

Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready 
WebSpace : westeuropewebspace
```

<span data-ttu-id="7784b-117">Det här kommandot hämtar webb värd planen med namnet Default0 i det webspace som heter westeuropewebspace i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="7784b-117">This command gets the web hosting plan named Default0 in the webspace named westeuropewebspace in the current subscription.</span></span>

## <span data-ttu-id="7784b-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7784b-118">PARAMETERS</span></span>

### <span data-ttu-id="7784b-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="7784b-119">-Name</span></span>
<span data-ttu-id="7784b-120">Anger namnet på en plan i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="7784b-120">Specifies the name of a plan in the subscription.</span></span>
<span data-ttu-id="7784b-121">Som standard får denna cmdlet alla planer i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="7784b-121">By default, this cmdlet gets all plans in the current subscription.</span></span>
<span data-ttu-id="7784b-122">Den här parametern stöder inte jokertecken.</span><span class="sxs-lookup"><span data-stu-id="7784b-122">This parameter does not support wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7784b-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="7784b-123">-Profile</span></span>
<span data-ttu-id="7784b-124">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="7784b-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7784b-125">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="7784b-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7784b-126">-WebSpaceName</span><span class="sxs-lookup"><span data-stu-id="7784b-126">-WebSpaceName</span></span>
<span data-ttu-id="7784b-127">Anger namnet på ett webbområde i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="7784b-127">Specifies the name of a webspace in the subscription.</span></span>
<span data-ttu-id="7784b-128">Som standard hämtar denna cmdlet alla webbplatser i angivet Webspace.</span><span class="sxs-lookup"><span data-stu-id="7784b-128">By default, this cmdlet gets all websites in the specified webspace.</span></span>
<span data-ttu-id="7784b-129">Den här parametern stöder inte jokertecken.</span><span class="sxs-lookup"><span data-stu-id="7784b-129">This parameter does not support wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7784b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7784b-130">CommonParameters</span></span>
<span data-ttu-id="7784b-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7784b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7784b-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7784b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7784b-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7784b-133">INPUTS</span></span>

###  
<span data-ttu-id="7784b-134">Du kan skicka data till denna cmdlet efter egenskaps namn, men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="7784b-134">You can pass input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="7784b-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7784b-135">OUTPUTS</span></span>

### <span data-ttu-id="7784b-136">Microsoft. WindowsAzure. commands. Utilities. webentities. WebHostingPlan</span><span class="sxs-lookup"><span data-stu-id="7784b-136">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.WebHostingPlan</span></span>
<span data-ttu-id="7784b-137">Som standard returnerar **Get-AzureWebHostingPlan** en matris med **WebHostingPlan** -objekt.</span><span class="sxs-lookup"><span data-stu-id="7784b-137">By default, **Get-AzureWebHostingPlan** returns an array of **WebHostingPlan** objects.</span></span>

## <span data-ttu-id="7784b-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7784b-138">NOTES</span></span>

## <span data-ttu-id="7784b-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7784b-139">RELATED LINKS</span></span>

