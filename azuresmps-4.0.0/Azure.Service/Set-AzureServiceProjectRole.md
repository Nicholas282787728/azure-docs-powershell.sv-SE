---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5D093C10-F8B6-4F4A-ABD7-CC4D7AB7AFFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: c78f53b95d18de600535368a1109b318294928c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099182"
---
# <span data-ttu-id="a1011-101">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="a1011-101">Set-AzureServiceProjectRole</span></span>

## <span data-ttu-id="a1011-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a1011-102">SYNOPSIS</span></span>
<span data-ttu-id="a1011-103">Anger antal instanser eller kör tids version för en roll.</span><span class="sxs-lookup"><span data-stu-id="a1011-103">Sets the number of instances or the runtime version of a role.</span></span>

## <span data-ttu-id="a1011-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a1011-104">SYNTAX</span></span>

### <span data-ttu-id="a1011-105">Ersätter</span><span class="sxs-lookup"><span data-stu-id="a1011-105">Instances</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] -Instances <Int32> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1011-106">Tidens</span><span class="sxs-lookup"><span data-stu-id="a1011-106">Runtime</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] -Runtime <String> -Version <String> [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a1011-107">VMSize</span><span class="sxs-lookup"><span data-stu-id="a1011-107">VMSize</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] [-PassThru] -VMSize <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1011-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a1011-108">DESCRIPTION</span></span>
<span data-ttu-id="a1011-109">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="a1011-109">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a1011-110">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a1011-110">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="a1011-111">Cmdleten **set-AzureServiceProjectRole** anger antalet roll instanser för den angivna rollen.</span><span class="sxs-lookup"><span data-stu-id="a1011-111">The **Set-AzureServiceProjectRole** cmdlet sets the number of role instances for the specified role.</span></span>

## <span data-ttu-id="a1011-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a1011-112">EXAMPLES</span></span>

### <span data-ttu-id="a1011-113">Exempel 1: Ange instanser för en webb roll</span><span class="sxs-lookup"><span data-stu-id="a1011-113">Example 1: Set instances for a web role</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyWebRole" 2
```

<span data-ttu-id="a1011-114">Anger antalet instanser för webb rollen med namnet MyWebRole1 till 2.</span><span class="sxs-lookup"><span data-stu-id="a1011-114">Sets the number of instances for the web role named MyWebRole1 to 2.</span></span>

### <span data-ttu-id="a1011-115">Exempel 2: Ange instanser för en arbets roll</span><span class="sxs-lookup"><span data-stu-id="a1011-115">Example 2: Set instances for a worker role</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyWorkerRole1" 2
```

<span data-ttu-id="a1011-116">Anger antalet roll instanser för arbets rollen som heter WorkerRole1 till 2.</span><span class="sxs-lookup"><span data-stu-id="a1011-116">Sets the role instance count for the worker role named WorkerRole1 to 2.</span></span>

### <span data-ttu-id="a1011-117">Exempel 3: Ange kör tids version för en roll tjänst</span><span class="sxs-lookup"><span data-stu-id="a1011-117">Example 3: Set the runtime version for a role service</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyRole1" node 0.6.20
```

<span data-ttu-id="a1011-118">Anger node.exe runtime-versionen för rollen MyRole1 till 0.6.20.</span><span class="sxs-lookup"><span data-stu-id="a1011-118">Sets the node.exe runtime version for role MyRole1 to 0.6.20.</span></span>

## <span data-ttu-id="a1011-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a1011-119">PARAMETERS</span></span>

### <span data-ttu-id="a1011-120">-Instanser</span><span class="sxs-lookup"><span data-stu-id="a1011-120">-Instances</span></span>
<span data-ttu-id="a1011-121">Anger antalet roll instanser för den angivna webb-eller jobb rollen.</span><span class="sxs-lookup"><span data-stu-id="a1011-121">Specifies the number of role instances for the specified web or worker role.</span></span>

```yaml
Type: Int32
Parameter Sets: Instances
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1011-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1011-122">-PassThru</span></span>
<span data-ttu-id="a1011-123">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="a1011-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a1011-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="a1011-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1011-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="a1011-125">-Profile</span></span>
<span data-ttu-id="a1011-126">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="a1011-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a1011-127">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="a1011-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a1011-128">-RoleName</span><span class="sxs-lookup"><span data-stu-id="a1011-128">-RoleName</span></span>
<span data-ttu-id="a1011-129">Anger namnet på den webb eller arbets roll som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="a1011-129">Specifies the name of the web or worker role to be changed.</span></span>

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

### <span data-ttu-id="a1011-130">-Runtime</span><span class="sxs-lookup"><span data-stu-id="a1011-130">-Runtime</span></span>
<span data-ttu-id="a1011-131">Anger hur du vill lägga till den angivna rollen.</span><span class="sxs-lookup"><span data-stu-id="a1011-131">Specifies the runtime to add to the specified role.</span></span>

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1011-132">-Version</span><span class="sxs-lookup"><span data-stu-id="a1011-132">-Version</span></span>
<span data-ttu-id="a1011-133">Anger den version av körnings miljön som ska läggas till i rollen.</span><span class="sxs-lookup"><span data-stu-id="a1011-133">Specifies the version of the runtime to add to the role.</span></span>

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1011-134">-VMSize</span><span class="sxs-lookup"><span data-stu-id="a1011-134">-VMSize</span></span>
<span data-ttu-id="a1011-135">Anger rollens virtuella dator storlek.</span><span class="sxs-lookup"><span data-stu-id="a1011-135">Specifies the virtual machine size of the role.</span></span>

```yaml
Type: String
Parameter Sets: VMSize
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1011-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1011-136">CommonParameters</span></span>
<span data-ttu-id="a1011-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1011-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1011-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1011-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1011-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a1011-139">INPUTS</span></span>

###  
<span data-ttu-id="a1011-140">Anger storleken på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="a1011-140">Specifies the size of the virtual machine.</span></span>

## <span data-ttu-id="a1011-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a1011-141">OUTPUTS</span></span>

## <span data-ttu-id="a1011-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a1011-142">NOTES</span></span>

## <span data-ttu-id="a1011-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a1011-143">RELATED LINKS</span></span>

[<span data-ttu-id="a1011-144">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="a1011-144">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)


