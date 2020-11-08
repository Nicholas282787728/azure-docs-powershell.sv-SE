---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D7EB9FE4-BDEB-43A5-B6D3-FEAB16BC2711
online version: ''
schema: 2.0.0
ms.openlocfilehash: 388277115281cbbacfb634ebdac5cdd9aa86b709
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100644"
---
# <span data-ttu-id="0a7f1-101">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="0a7f1-101">Get-WAPackVMRole</span></span>

## <span data-ttu-id="0a7f1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0a7f1-102">SYNOPSIS</span></span>

## <span data-ttu-id="0a7f1-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0a7f1-103">SYNTAX</span></span>

### <span data-ttu-id="0a7f1-104">Tom (standard)</span><span class="sxs-lookup"><span data-stu-id="0a7f1-104">Empty (Default)</span></span>
```
Get-WAPackVMRole [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0a7f1-105">FromName</span><span class="sxs-lookup"><span data-stu-id="0a7f1-105">FromName</span></span>
```
Get-WAPackVMRole -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0a7f1-106">FromCloudService</span><span class="sxs-lookup"><span data-stu-id="0a7f1-106">FromCloudService</span></span>
```
Get-WAPackVMRole -Name <String> -CloudServiceName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0a7f1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0a7f1-107">DESCRIPTION</span></span>
<span data-ttu-id="0a7f1-108">De här ämnena är föråldrade och kommer att tas bort i framtiden.</span><span class="sxs-lookup"><span data-stu-id="0a7f1-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="0a7f1-109">I det här avsnittet beskrivs cmdleten i 0.8.1-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="0a7f1-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0a7f1-110">För att ta reda på vilken version av modulen du använder, går du till Azure PowerShell-konsolen och skriver `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="0a7f1-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="0a7f1-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0a7f1-111">EXAMPLES</span></span>

### <span data-ttu-id="0a7f1-112">Exempel 1: skaffa en virtuell dator roll (skapad via portalen)</span><span class="sxs-lookup"><span data-stu-id="0a7f1-112">Example 1: Get a virtual machine role (created through the portal)</span></span>
```
PS C:\> Get-WAPackVMRole -Name "ContosoVMRole01"
```

<span data-ttu-id="0a7f1-113">Det här kommandot får en virtuell dator roll som har skapats via portalen med namnet ContosoVMRole01.</span><span class="sxs-lookup"><span data-stu-id="0a7f1-113">This command gets a virtual machine role which has been created through the portal named ContosoVMRole01.</span></span>

### <span data-ttu-id="0a7f1-114">Exempel 2: skaffa en virtuell dator roll genom att använda ett namn och ett namn på en moln tjänst</span><span class="sxs-lookup"><span data-stu-id="0a7f1-114">Example 2: Get a virtual machine role by using a name and a cloud service name</span></span>
```
PS C:\> Get-WAPackVMRole -CloudServiceName "ContosoCloudService01" -Name "ContosoVMRole02"
```

<span data-ttu-id="0a7f1-115">Det här kommandot får rollen som virtuell dator med namnet ContosoVMRole02 som står på en moln tjänst med namnet ContosoCloudService01.</span><span class="sxs-lookup"><span data-stu-id="0a7f1-115">This command gets a virtual machine role named ContosoVMRole02 which stand on a cloud service named ContosoCloudService01.</span></span>

### <span data-ttu-id="0a7f1-116">Exempel 3: Hämta alla virtuella dator roller</span><span class="sxs-lookup"><span data-stu-id="0a7f1-116">Example 3: Get all virtual machine role</span></span>
```
PS C:\> Get-WAPackVMRole
```

<span data-ttu-id="0a7f1-117">Det här kommandot får alla befintliga virtuella dator roller.</span><span class="sxs-lookup"><span data-stu-id="0a7f1-117">This command gets all existing virtual machine role.</span></span>

## <span data-ttu-id="0a7f1-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0a7f1-118">PARAMETERS</span></span>

### <span data-ttu-id="0a7f1-119">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="0a7f1-119">-CloudServiceName</span></span>
<span data-ttu-id="0a7f1-120">Anger namnet på den virtuella datorns moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="0a7f1-120">Specifies the cloud service name of virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a7f1-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="0a7f1-121">-Name</span></span>
<span data-ttu-id="0a7f1-122">Anger namnet på en virtuell dator roll.</span><span class="sxs-lookup"><span data-stu-id="0a7f1-122">Specifies the name of a virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: FromName, FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a7f1-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="0a7f1-123">-Profile</span></span>
<span data-ttu-id="0a7f1-124">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="0a7f1-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0a7f1-125">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="0a7f1-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0a7f1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a7f1-126">CommonParameters</span></span>
<span data-ttu-id="0a7f1-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a7f1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a7f1-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a7f1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a7f1-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0a7f1-129">INPUTS</span></span>

## <span data-ttu-id="0a7f1-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0a7f1-130">OUTPUTS</span></span>

## <span data-ttu-id="0a7f1-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0a7f1-131">NOTES</span></span>

## <span data-ttu-id="0a7f1-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0a7f1-132">RELATED LINKS</span></span>

[<span data-ttu-id="0a7f1-133">New-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="0a7f1-133">New-WAPackVMRole</span></span>](./New-WAPackVMRole.md)

[<span data-ttu-id="0a7f1-134">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="0a7f1-134">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)

[<span data-ttu-id="0a7f1-135">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="0a7f1-135">Set-WAPackVMRole</span></span>](./Set-WAPackVMRole.md)


