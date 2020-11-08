---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 453AEA42-E29C-4FF2-9210-0DD88B77DC07
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29c7f8bc814ddf5295064d89eeaf34c8e7274916
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099738"
---
# <span data-ttu-id="3328f-101">Get-WAPackCloudVMRoleSizeProfile</span><span class="sxs-lookup"><span data-stu-id="3328f-101">Get-WAPackCloudVMRoleSizeProfile</span></span>

## <span data-ttu-id="3328f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3328f-102">SYNOPSIS</span></span>
<span data-ttu-id="3328f-103">Hämtar profil objekt för den virtuella dator rollen.</span><span class="sxs-lookup"><span data-stu-id="3328f-103">Gets Cloud VM Role Size profile objects.</span></span>

## <span data-ttu-id="3328f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3328f-104">SYNTAX</span></span>

### <span data-ttu-id="3328f-105">Tom (standard)</span><span class="sxs-lookup"><span data-stu-id="3328f-105">Empty (Default)</span></span>
```
Get-WAPackCloudVMRoleSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3328f-106">FromName</span><span class="sxs-lookup"><span data-stu-id="3328f-106">FromName</span></span>
```
Get-WAPackCloudVMRoleSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3328f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3328f-107">DESCRIPTION</span></span>
<span data-ttu-id="3328f-108">Cmdleten **Get-WAPackCloudVMRoleSizeProfile** hämtar den virtuella dator rollens storleks profil objekt för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="3328f-108">The **Get-WAPackCloudVMRoleSizeProfile** cmdlet gets Cloud VM Role size profile objects for virtual machines.</span></span>

## <span data-ttu-id="3328f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3328f-109">EXAMPLES</span></span>

### <span data-ttu-id="3328f-110">Exempel 1: skaffa en profil för den virtuella dator rollen för en moln genom att använda ett namn</span><span class="sxs-lookup"><span data-stu-id="3328f-110">Example 1: Get a Cloud VM Role size profile by using a name</span></span>
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile -Name "Small"
```

<span data-ttu-id="3328f-111">Det här kommandot får storleks profilen liten.</span><span class="sxs-lookup"><span data-stu-id="3328f-111">This command gets the size profile named Small.</span></span>

### <span data-ttu-id="3328f-112">Exempel 2: Hämta alla storleks profiler för rollen virtuella dator roller</span><span class="sxs-lookup"><span data-stu-id="3328f-112">Example 2: Get all Cloud VM Role size profiles</span></span>
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile
```

<span data-ttu-id="3328f-113">Det här kommandot får alla storleks profiler.</span><span class="sxs-lookup"><span data-stu-id="3328f-113">This command gets all the size profiles.</span></span>

## <span data-ttu-id="3328f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3328f-114">PARAMETERS</span></span>

### <span data-ttu-id="3328f-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="3328f-115">-Name</span></span>
<span data-ttu-id="3328f-116">Anger namnet på en profil för den virtuella dator rollen.</span><span class="sxs-lookup"><span data-stu-id="3328f-116">Specifies the name of a Cloud VM Role size profile.</span></span>

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

### <span data-ttu-id="3328f-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="3328f-117">-Profile</span></span>
<span data-ttu-id="3328f-118">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="3328f-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3328f-119">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="3328f-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3328f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3328f-120">CommonParameters</span></span>
<span data-ttu-id="3328f-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3328f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3328f-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3328f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3328f-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3328f-123">INPUTS</span></span>

## <span data-ttu-id="3328f-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3328f-124">OUTPUTS</span></span>

## <span data-ttu-id="3328f-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3328f-125">NOTES</span></span>

## <span data-ttu-id="3328f-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3328f-126">RELATED LINKS</span></span>

[<span data-ttu-id="3328f-127">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="3328f-127">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


