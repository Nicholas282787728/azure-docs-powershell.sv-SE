---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FB5CD696-108D-4A3E-8983-1C6562E8795A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25ade8ccf395d37ab0856742fe473a6508c9d63b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093437"
---
# <span data-ttu-id="e1d09-101">Add-AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="e1d09-101">Add-AzureWebRole</span></span>

## <span data-ttu-id="e1d09-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e1d09-102">SYNOPSIS</span></span>
<span data-ttu-id="e1d09-103">Lägger till en webb roll.</span><span class="sxs-lookup"><span data-stu-id="e1d09-103">Adds a web worker role.</span></span>

## <span data-ttu-id="e1d09-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e1d09-104">SYNTAX</span></span>

```
Add-AzureWebRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1d09-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e1d09-105">DESCRIPTION</span></span>
<span data-ttu-id="e1d09-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="e1d09-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e1d09-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e1d09-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e1d09-108">Cmdleten **Add-AzureWebRole** lägger till en webb jobb roll.</span><span class="sxs-lookup"><span data-stu-id="e1d09-108">The **Add-AzureWebRole** cmdlet adds a web worker role.</span></span>

## <span data-ttu-id="e1d09-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e1d09-109">EXAMPLES</span></span>

### <span data-ttu-id="e1d09-110">Exempel 1: lägga till en standard roll</span><span class="sxs-lookup"><span data-stu-id="e1d09-110">Example 1: Add a default role</span></span>
```
PS C:\> Add-AzureWebRole
```

<span data-ttu-id="e1d09-111">Det här kommandot Lägg till webb roll med standard konfigurationen för Webrole1 som namnet och en enda instans.</span><span class="sxs-lookup"><span data-stu-id="e1d09-111">This command add web role that has the default configuration of Webrole1 as the name and a single instance.</span></span>

### <span data-ttu-id="e1d09-112">Exempel 2: lägga till en roll med ett namn</span><span class="sxs-lookup"><span data-stu-id="e1d09-112">Example 2: Add a role with a name</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole"
```

<span data-ttu-id="e1d09-113">Det här kommandot lägger till en enskild webb roll med namnet MyWebRole i det aktuella programmet.</span><span class="sxs-lookup"><span data-stu-id="e1d09-113">This command adds a single web role named MyWebRole to the current application.</span></span>

### <span data-ttu-id="e1d09-114">Exempel 3: lägga till en roll med namn och instans antal</span><span class="sxs-lookup"><span data-stu-id="e1d09-114">Example 3: Add a role with a name and instance count</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -Instance 2
```

<span data-ttu-id="e1d09-115">Det här kommandot lägger till en webb roll med namnet MyWebRole i det aktuella programmet.</span><span class="sxs-lookup"><span data-stu-id="e1d09-115">This command adds a web role named MyWebRole to the current application.</span></span>
<span data-ttu-id="e1d09-116">Cmdleten har en roll instans räkning på 2.</span><span class="sxs-lookup"><span data-stu-id="e1d09-116">The cmdlet has a role instance count of 2.</span></span>

### <span data-ttu-id="e1d09-117">Exempel 4: lägga till en roll med ett namn och en mall</span><span class="sxs-lookup"><span data-stu-id="e1d09-117">Example 4: Add a role with a name and template</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -TemplateFolder ".\MyWebTemplateFolder"
```

<span data-ttu-id="e1d09-118">Det här kommandot lägger till en enskild webb roll med namnet MyWebRole i det aktuella programmet.</span><span class="sxs-lookup"><span data-stu-id="e1d09-118">This command adds a single web role named MyWebRole to the current application.</span></span>
<span data-ttu-id="e1d09-119">Kommandot anger en mapp med namnet MyWebTemplateFolder som en scaffolding-mall.</span><span class="sxs-lookup"><span data-stu-id="e1d09-119">The command specifies a folder named MyWebTemplateFolder as a scaffolding template.</span></span>

## <span data-ttu-id="e1d09-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e1d09-120">PARAMETERS</span></span>

### <span data-ttu-id="e1d09-121">-Instanser</span><span class="sxs-lookup"><span data-stu-id="e1d09-121">-Instances</span></span>
<span data-ttu-id="e1d09-122">Anger antalet instanser.</span><span class="sxs-lookup"><span data-stu-id="e1d09-122">Specifies the number of instances.</span></span>

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

### <span data-ttu-id="e1d09-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="e1d09-123">-Name</span></span>
<span data-ttu-id="e1d09-124">Anger namnet på webb rollen.</span><span class="sxs-lookup"><span data-stu-id="e1d09-124">Specifies the name of the web role.</span></span>

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

### <span data-ttu-id="e1d09-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="e1d09-125">-Profile</span></span>
<span data-ttu-id="e1d09-126">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="e1d09-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e1d09-127">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="e1d09-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e1d09-128">-TemplateFolder</span><span class="sxs-lookup"><span data-stu-id="e1d09-128">-TemplateFolder</span></span>
<span data-ttu-id="e1d09-129">Anger mappen för mallen.</span><span class="sxs-lookup"><span data-stu-id="e1d09-129">Specifies the template folder.</span></span>

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

### <span data-ttu-id="e1d09-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d09-130">CommonParameters</span></span>
<span data-ttu-id="e1d09-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1d09-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d09-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1d09-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d09-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e1d09-133">INPUTS</span></span>

## <span data-ttu-id="e1d09-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e1d09-134">OUTPUTS</span></span>

## <span data-ttu-id="e1d09-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e1d09-135">NOTES</span></span>

## <span data-ttu-id="e1d09-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e1d09-136">RELATED LINKS</span></span>

[<span data-ttu-id="e1d09-137">Add-AzureWorkerRole</span><span class="sxs-lookup"><span data-stu-id="e1d09-137">Add-AzureWorkerRole</span></span>](./Add-AzureWorkerRole.md)

[<span data-ttu-id="e1d09-138">New-AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="e1d09-138">New-AzureRoleTemplate</span></span>](./New-AzureRoleTemplate.md)


