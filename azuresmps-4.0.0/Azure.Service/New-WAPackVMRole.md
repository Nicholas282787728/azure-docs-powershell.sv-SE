---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6617AA59-CDD1-4BA9-84A7-F3914BF1D4B7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 14e201dc916f15b63b0e825f4ca2e37015aaa9bc
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100620"
---
# <span data-ttu-id="ed024-101">New-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="ed024-101">New-WAPackVMRole</span></span>

## <span data-ttu-id="ed024-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed024-102">SYNOPSIS</span></span>
<span data-ttu-id="ed024-103">Skapar en virtuell dator roll.</span><span class="sxs-lookup"><span data-stu-id="ed024-103">Creates a virtual machine role.</span></span>

## <span data-ttu-id="ed024-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed024-104">SYNTAX</span></span>

### <span data-ttu-id="ed024-105">QuickCreate (standard)</span><span class="sxs-lookup"><span data-stu-id="ed024-105">QuickCreate (Default)</span></span>
```
New-WAPackVMRole -Name <String> -Label <String> -ResourceDefinition <VMRoleResourceDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ed024-106">FromCloudService</span><span class="sxs-lookup"><span data-stu-id="ed024-106">FromCloudService</span></span>
```
New-WAPackVMRole -Name <String> -Label <String> -ResourceDefinition <VMRoleResourceDefinition>
 -CloudService <CloudService> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ed024-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed024-107">DESCRIPTION</span></span>
<span data-ttu-id="ed024-108">De här ämnena är föråldrade och kommer att tas bort i framtiden.</span><span class="sxs-lookup"><span data-stu-id="ed024-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="ed024-109">I det här avsnittet beskrivs cmdleten i 0.8.1-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="ed024-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ed024-110">För att ta reda på vilken version av modulen du använder, går du till Azure PowerShell-konsolen och skriver `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ed024-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ed024-111">Cmdleten **New-WAPackVMRole** skapar en roll för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="ed024-111">The **New-WAPackVMRole** cmdlet creates a virtual machine role.</span></span>

## <span data-ttu-id="ed024-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed024-112">EXAMPLES</span></span>

### <span data-ttu-id="ed024-113">Exempel 1: skapa en virtuell dator roll (emulering av WAP)</span><span class="sxs-lookup"><span data-stu-id="ed024-113">Example 1: Create a virtual machine role (emulating WAP behavior)</span></span>
```
PS C:\> New-WAPackVMRole -Name "ContosoVMRole01" -Label "ContosoVMRoleLabel01" -ResourceDefinition $resdef
```

<span data-ttu-id="ed024-114">Eftersom vi inte anger någon moln tjänst (emulering med WAP) skapar kommandot en moln tjänst åt oss som har samma namn som den virtuella dator rollen.</span><span class="sxs-lookup"><span data-stu-id="ed024-114">Since we do not specify any cloud service (emulating WAP behavior), the command will create a cloud service for us which will have the same name as the virtual machine role.</span></span>
<span data-ttu-id="ed024-115">I det här fallet skapar följande kommando rollen virtuell dator med namnet ContosoVMRole01, Label ContosoVMRoleLabel01.</span><span class="sxs-lookup"><span data-stu-id="ed024-115">In this case, the following command will create a virtual machine role with the name ContosoVMRole01, label ContosoVMRoleLabel01.</span></span>
<span data-ttu-id="ed024-116">Observera att den resurs definition som används här måste skapas manuellt med PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ed024-116">Note that the resource definition being used here has to be manually created though PowerShell.</span></span>

## <span data-ttu-id="ed024-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed024-117">PARAMETERS</span></span>

### <span data-ttu-id="ed024-118">-CloudService</span><span class="sxs-lookup"><span data-stu-id="ed024-118">-CloudService</span></span>
<span data-ttu-id="ed024-119">Anger en moln tjänst för rollen virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="ed024-119">Specifies a cloud service for the virtual machine role.</span></span>

```yaml
Type: CloudService
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed024-120">-Etikett</span><span class="sxs-lookup"><span data-stu-id="ed024-120">-Label</span></span>
<span data-ttu-id="ed024-121">Anger en etikett för den virtuella dator rollen.</span><span class="sxs-lookup"><span data-stu-id="ed024-121">Specifies a label for the virtual machine role.</span></span>

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

### <span data-ttu-id="ed024-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="ed024-122">-Name</span></span>
<span data-ttu-id="ed024-123">Anger ett namn för den virtuella dator rollen.</span><span class="sxs-lookup"><span data-stu-id="ed024-123">Specifies a name for the virtual machine role.</span></span>

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

### <span data-ttu-id="ed024-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="ed024-124">-Profile</span></span>
<span data-ttu-id="ed024-125">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="ed024-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ed024-126">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="ed024-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ed024-127">-ResourceDefinition</span><span class="sxs-lookup"><span data-stu-id="ed024-127">-ResourceDefinition</span></span>
<span data-ttu-id="ed024-128">Anger en resurs definition för rollen virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="ed024-128">Specifies a resource definition for the virtual machine role.</span></span>

```yaml
Type: VMRoleResourceDefinition
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed024-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed024-129">CommonParameters</span></span>
<span data-ttu-id="ed024-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed024-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed024-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed024-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed024-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed024-132">INPUTS</span></span>

## <span data-ttu-id="ed024-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed024-133">OUTPUTS</span></span>

## <span data-ttu-id="ed024-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed024-134">NOTES</span></span>

## <span data-ttu-id="ed024-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed024-135">RELATED LINKS</span></span>

[<span data-ttu-id="ed024-136">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="ed024-136">Get-WAPackVMRole</span></span>](./Get-WAPackVMRole.md)

[<span data-ttu-id="ed024-137">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="ed024-137">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)

[<span data-ttu-id="ed024-138">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="ed024-138">Set-WAPackVMRole</span></span>](./Set-WAPackVMRole.md)


