---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 3EC274C9-9BF6-4B39-BC70-C7F9D780805D
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4081d6d072aadd6a4ae7d09ff57748a8f2cb697
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093306"
---
# <span data-ttu-id="a898f-101">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="a898f-101">Get-AzureSiteRecoveryServer</span></span>

## <span data-ttu-id="a898f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a898f-102">SYNOPSIS</span></span>
<span data-ttu-id="a898f-103">Får webbplats återställnings servrar registrerade ett återställnings valv för webbplatser.</span><span class="sxs-lookup"><span data-stu-id="a898f-103">Gets Site Recovery servers registered a Site Recovery vault.</span></span>

## <span data-ttu-id="a898f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a898f-104">SYNTAX</span></span>

### <span data-ttu-id="a898f-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="a898f-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryServer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a898f-106">ById</span><span class="sxs-lookup"><span data-stu-id="a898f-106">ById</span></span>
```
Get-AzureSiteRecoveryServer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a898f-107">ByName</span><span class="sxs-lookup"><span data-stu-id="a898f-107">ByName</span></span>
```
Get-AzureSiteRecoveryServer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a898f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a898f-108">DESCRIPTION</span></span>
<span data-ttu-id="a898f-109">Cmdleten **Get-AzureSiteRecoveryServer** hämtar information om Azure Site Recovery-servrar registrerade till det aktuella Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="a898f-109">The **Get-AzureSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="a898f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a898f-110">EXAMPLES</span></span>

### <span data-ttu-id="a898f-111">Exempel 1: Hämta information om en webbplats återställnings Server</span><span class="sxs-lookup"><span data-stu-id="a898f-111">Example 1: Get information about a Site Recovery server</span></span>
```
PS C:\> Get-AzureSiteRecoveryServer
ID              : cd7dec80-1144-4531-9ab3-888b8ab39bee
Name            : server1.contoso.com
LastHeartbeat   : 9/23/2014 3:51:22 PM
ProviderVersion : 3.5.520.0
ServerVersion   : 3.2.7634.0

ID              : f5e713fe-5b6d-4641-9690-6fe74c976b8e
Name            : Server2.contoso.com
LastHeartbeat   : 8/13/2014 2:28:58 PM
ProviderVersion : 3.5
ServerVersion   : 3.2.7510.0
```

<span data-ttu-id="a898f-112">Det här kommandot får information om en Azure Site Recovery-Server.</span><span class="sxs-lookup"><span data-stu-id="a898f-112">This command gets information about an Azure Site Recovery server.</span></span>

## <span data-ttu-id="a898f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a898f-113">PARAMETERS</span></span>

### <span data-ttu-id="a898f-114">-ID</span><span class="sxs-lookup"><span data-stu-id="a898f-114">-Id</span></span>
<span data-ttu-id="a898f-115">Anger ID för en server.</span><span class="sxs-lookup"><span data-stu-id="a898f-115">Specifies the ID of a server.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a898f-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="a898f-116">-Name</span></span>
<span data-ttu-id="a898f-117">Anger namnet på en server.</span><span class="sxs-lookup"><span data-stu-id="a898f-117">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a898f-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="a898f-118">-Profile</span></span>
<span data-ttu-id="a898f-119">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="a898f-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a898f-120">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="a898f-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a898f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a898f-121">CommonParameters</span></span>
<span data-ttu-id="a898f-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a898f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a898f-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a898f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a898f-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a898f-124">INPUTS</span></span>

## <span data-ttu-id="a898f-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a898f-125">OUTPUTS</span></span>

## <span data-ttu-id="a898f-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a898f-126">NOTES</span></span>

## <span data-ttu-id="a898f-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a898f-127">RELATED LINKS</span></span>

[<span data-ttu-id="a898f-128">Azure Site Recovery Services-cmdletar</span><span class="sxs-lookup"><span data-stu-id="a898f-128">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


