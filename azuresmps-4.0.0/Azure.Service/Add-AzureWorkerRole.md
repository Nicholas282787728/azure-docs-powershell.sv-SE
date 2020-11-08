---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8632A865-D4CC-4AE5-8307-055CDD776D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b79ee50bb5097896c2a120a9b7316adb2146b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093436"
---
# <span data-ttu-id="6539d-101">Add-AzureWorkerRole</span><span class="sxs-lookup"><span data-stu-id="6539d-101">Add-AzureWorkerRole</span></span>

## <span data-ttu-id="6539d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6539d-102">SYNOPSIS</span></span>
<span data-ttu-id="6539d-103">Skapar nödvändiga filer och konfiguration för en anpassad arbets roll.</span><span class="sxs-lookup"><span data-stu-id="6539d-103">Creates required files and configuration for a custom worker role.</span></span>

## <span data-ttu-id="6539d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6539d-104">SYNTAX</span></span>

```
Add-AzureWorkerRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6539d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6539d-105">DESCRIPTION</span></span>
<span data-ttu-id="6539d-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="6539d-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="6539d-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="6539d-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="6539d-108">Cmdleten **Add-AzureWorkerRole** skapar nödvändiga filer och konfigurationer, som ibland kallas scaffolding, för en anpassad arbets roll.</span><span class="sxs-lookup"><span data-stu-id="6539d-108">The **Add-AzureWorkerRole** cmdlet creates required files and configuration, sometimes referred to as scaffolding, for a custom worker role.</span></span>

## <span data-ttu-id="6539d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6539d-109">EXAMPLES</span></span>

### <span data-ttu-id="6539d-110">Exempel 1: skapa en enskild instans arbets roll</span><span class="sxs-lookup"><span data-stu-id="6539d-110">Example 1: Create a single instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole -Name MyWorkerRole
```

<span data-ttu-id="6539d-111">I det här exemplet läggs scaffolding för en arbets roll som heter MyWorkerRole till det aktuella programmet.</span><span class="sxs-lookup"><span data-stu-id="6539d-111">This example adds scaffolding for a single worker role named MyWorkerRole to the current application.</span></span>

### <span data-ttu-id="6539d-112">Exempel 2: skapa en roll för flera instanser</span><span class="sxs-lookup"><span data-stu-id="6539d-112">Example 2: Create a multiple instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -I 2
```

<span data-ttu-id="6539d-113">I det här exemplet läggs scaffolding till för en ny arbets roll som heter MyWorkerRole i det aktuella programmet, med antal roller på en roll instans.</span><span class="sxs-lookup"><span data-stu-id="6539d-113">This example adds scaffolding for a new worker role named MyWorkerRole to the current application, with a role instance count of 2.</span></span>

### <span data-ttu-id="6539d-114">Exempel 3: skapa arbets roll med anpassade scaffolding</span><span class="sxs-lookup"><span data-stu-id="6539d-114">Example 3: Create worker role with custom scaffolding</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -TemplateFoldr .\MyWorkerRoleTemplate
```

<span data-ttu-id="6539d-115">I det här exemplet skapas en arbets roll med anpassade scaffolding.</span><span class="sxs-lookup"><span data-stu-id="6539d-115">This example creates a worker role with custom scaffolding.</span></span>

## <span data-ttu-id="6539d-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6539d-116">PARAMETERS</span></span>

### <span data-ttu-id="6539d-117">-Instanser</span><span class="sxs-lookup"><span data-stu-id="6539d-117">-Instances</span></span>
<span data-ttu-id="6539d-118">Anger antalet roll instanser för denna arbets roll.</span><span class="sxs-lookup"><span data-stu-id="6539d-118">Specifies the number of role instances for this worker role.</span></span>
<span data-ttu-id="6539d-119">Standardvärdet är 1.</span><span class="sxs-lookup"><span data-stu-id="6539d-119">The default is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6539d-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="6539d-120">-Name</span></span>
<span data-ttu-id="6539d-121">Anger namnet på arbets rollen.</span><span class="sxs-lookup"><span data-stu-id="6539d-121">Specifies the name of the worker role.</span></span>
<span data-ttu-id="6539d-122">Det här värdet bestämmer mappnamnet som innehåller scaffolding för det anpassade program som finns i arbets rollen.</span><span class="sxs-lookup"><span data-stu-id="6539d-122">This value determines the folder name that contains the scaffolding for the custom application that will be hosted in the worker role.</span></span>
<span data-ttu-id="6539d-123">Standardvärdet är WorkerRolenumber, där tal är antalet arbets roller i tjänsten.</span><span class="sxs-lookup"><span data-stu-id="6539d-123">The default is WorkerRolenumber, where number is the number of worker roles in the service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6539d-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="6539d-124">-Profile</span></span>
<span data-ttu-id="6539d-125">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="6539d-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6539d-126">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="6539d-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6539d-127">-TemplateFolder</span><span class="sxs-lookup"><span data-stu-id="6539d-127">-TemplateFolder</span></span>
<span data-ttu-id="6539d-128">Anger den scaffolding som ska användas för att skapa arbets rollen.</span><span class="sxs-lookup"><span data-stu-id="6539d-128">Specifies the scaffolding template folder to be used to create the worker role.</span></span>

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

### <span data-ttu-id="6539d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6539d-129">CommonParameters</span></span>
<span data-ttu-id="6539d-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6539d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6539d-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6539d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6539d-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6539d-132">INPUTS</span></span>

## <span data-ttu-id="6539d-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6539d-133">OUTPUTS</span></span>

## <span data-ttu-id="6539d-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6539d-134">NOTES</span></span>

## <span data-ttu-id="6539d-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6539d-135">RELATED LINKS</span></span>

[<span data-ttu-id="6539d-136">Add-AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="6539d-136">Add-AzureWebRole</span></span>](./Add-AzureWebRole.md)

[<span data-ttu-id="6539d-137">New-AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="6539d-137">New-AzureRoleTemplate</span></span>](./New-AzureRoleTemplate.md)


