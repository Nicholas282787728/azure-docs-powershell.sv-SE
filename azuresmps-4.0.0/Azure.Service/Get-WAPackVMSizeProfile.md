---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 48211644-1B92-443D-A992-BDF517D89341
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49b4039e07cf9f393a85c9592598ad870586fd06
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100660"
---
# <span data-ttu-id="7ba6f-101">Get-WAPackVMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="7ba6f-101">Get-WAPackVMSizeProfile</span></span>

## <span data-ttu-id="7ba6f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7ba6f-102">SYNOPSIS</span></span>
<span data-ttu-id="7ba6f-103">Ändrar profilernas storlek.</span><span class="sxs-lookup"><span data-stu-id="7ba6f-103">Gets size profile objects.</span></span>

## <span data-ttu-id="7ba6f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7ba6f-104">SYNTAX</span></span>

### <span data-ttu-id="7ba6f-105">Tom (standard)</span><span class="sxs-lookup"><span data-stu-id="7ba6f-105">Empty (Default)</span></span>
```
Get-WAPackVMSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7ba6f-106">FromId</span><span class="sxs-lookup"><span data-stu-id="7ba6f-106">FromId</span></span>
```
Get-WAPackVMSizeProfile [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7ba6f-107">FromName</span><span class="sxs-lookup"><span data-stu-id="7ba6f-107">FromName</span></span>
```
Get-WAPackVMSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7ba6f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7ba6f-108">DESCRIPTION</span></span>
<span data-ttu-id="7ba6f-109">De här ämnena är föråldrade och kommer att tas bort i framtiden.</span><span class="sxs-lookup"><span data-stu-id="7ba6f-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="7ba6f-110">I det här avsnittet beskrivs cmdleten i 0.8.1-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="7ba6f-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7ba6f-111">För att ta reda på vilken version av modulen du använder, går du till Azure PowerShell-konsolen och skriver `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="7ba6f-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7ba6f-112">Cmdleten **Get-WAPackVMSizeProfile** ändrar storlek på profil objekt för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="7ba6f-112">The **Get-WAPackVMSizeProfile** cmdlet gets size profile objects for virtual machines.</span></span>

## <span data-ttu-id="7ba6f-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7ba6f-113">EXAMPLES</span></span>

### <span data-ttu-id="7ba6f-114">Exempel 1: få en storleks profil genom att använda ett namn</span><span class="sxs-lookup"><span data-stu-id="7ba6f-114">Example 1: Get a size profile by using a name</span></span>
```
PS C:\> Get-WAPackVMSizeProfile -Name "ContosoSizeProfile07"
```

<span data-ttu-id="7ba6f-115">Det här kommandot får storleks profilen ContosoSizeProfile07.</span><span class="sxs-lookup"><span data-stu-id="7ba6f-115">This command gets the size profile named ContosoSizeProfile07.</span></span>

### <span data-ttu-id="7ba6f-116">Exempel 2: skapa en storleks profil med hjälp av ett ID</span><span class="sxs-lookup"><span data-stu-id="7ba6f-116">Example 2: Get a size profile by using an ID</span></span>
```
PS C:\> Get-WAPackVMSizeProfile -ID 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="7ba6f-117">Det här kommandot får storleks profilen med angivet ID.</span><span class="sxs-lookup"><span data-stu-id="7ba6f-117">This command gets the size profile that has the specified ID.</span></span>

### <span data-ttu-id="7ba6f-118">Exempel 3: Hämta alla storleks profiler</span><span class="sxs-lookup"><span data-stu-id="7ba6f-118">Example 3: Get all size profiles</span></span>
```
PS C:\> Get-WAPackVMSizeProfile
```

<span data-ttu-id="7ba6f-119">Det här kommandot får alla storleks profiler.</span><span class="sxs-lookup"><span data-stu-id="7ba6f-119">This command gets all the size profiles.</span></span>

## <span data-ttu-id="7ba6f-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7ba6f-120">PARAMETERS</span></span>

### <span data-ttu-id="7ba6f-121">-ID</span><span class="sxs-lookup"><span data-stu-id="7ba6f-121">-ID</span></span>
<span data-ttu-id="7ba6f-122">Anger ett unikt ID för en storleks profil.</span><span class="sxs-lookup"><span data-stu-id="7ba6f-122">Specifies the unique ID of a size profile.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ba6f-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="7ba6f-123">-Name</span></span>
<span data-ttu-id="7ba6f-124">Anger namnet på en storleks profil.</span><span class="sxs-lookup"><span data-stu-id="7ba6f-124">Specifies the name of a size profile.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ba6f-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="7ba6f-125">-Profile</span></span>
<span data-ttu-id="7ba6f-126">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="7ba6f-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7ba6f-127">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="7ba6f-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7ba6f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ba6f-128">CommonParameters</span></span>
<span data-ttu-id="7ba6f-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ba6f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ba6f-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ba6f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ba6f-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7ba6f-131">INPUTS</span></span>

## <span data-ttu-id="7ba6f-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7ba6f-132">OUTPUTS</span></span>

## <span data-ttu-id="7ba6f-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7ba6f-133">NOTES</span></span>

## <span data-ttu-id="7ba6f-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7ba6f-134">RELATED LINKS</span></span>

[<span data-ttu-id="7ba6f-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7ba6f-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


