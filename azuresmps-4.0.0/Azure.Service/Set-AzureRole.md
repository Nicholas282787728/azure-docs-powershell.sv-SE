---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8170AEF9-46E6-4087-8A68-29DFD5D014B5
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb63d143ca2cafce92109e17fd3ced6a9dc070e8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099054"
---
# <span data-ttu-id="24ee0-101">Set-AzureRole</span><span class="sxs-lookup"><span data-stu-id="24ee0-101">Set-AzureRole</span></span>

## <span data-ttu-id="24ee0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="24ee0-102">SYNOPSIS</span></span>
<span data-ttu-id="24ee0-103">Anger antalet instanser av en Azure-roll som ska köras.</span><span class="sxs-lookup"><span data-stu-id="24ee0-103">Sets the number of instances of an Azure role to run.</span></span>

## <span data-ttu-id="24ee0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="24ee0-104">SYNTAX</span></span>

```
Set-AzureRole [-ServiceName] <String> [-Slot] <String> [-RoleName] <String> [-Count] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="24ee0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="24ee0-105">DESCRIPTION</span></span>
<span data-ttu-id="24ee0-106">Cmdleten **set-AzureRole** anger antalet instanser av en viss roll som ska köras i en Azure-distribution.</span><span class="sxs-lookup"><span data-stu-id="24ee0-106">The **Set-AzureRole** cmdlet sets the number of instances of a specified role to run in an Azure deployment.</span></span>

## <span data-ttu-id="24ee0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="24ee0-107">EXAMPLES</span></span>

### <span data-ttu-id="24ee0-108">1: Ange antalet instanser för en roll</span><span class="sxs-lookup"><span data-stu-id="24ee0-108">1: Set the number of instances for a role</span></span>
```
PS C:\> Set-AzureRole -ServiceName "MySvc01" -Slot "Production" -RoleName "MyTestRole03" -Count 3
```

<span data-ttu-id="24ee0-109">Det här kommandot anger att MyTestRole03-rollen som körs i produktion på MySvc01-tjänsten ska ha tre instanser.</span><span class="sxs-lookup"><span data-stu-id="24ee0-109">This command sets the MyTestRole03 role that is running in production on the MySvc01 service to have three instances.</span></span>

## <span data-ttu-id="24ee0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="24ee0-110">PARAMETERS</span></span>

### <span data-ttu-id="24ee0-111">-Antal</span><span class="sxs-lookup"><span data-stu-id="24ee0-111">-Count</span></span>
<span data-ttu-id="24ee0-112">Anger antalet roll instanser som ska köras.</span><span class="sxs-lookup"><span data-stu-id="24ee0-112">Specifies the number of role instances to run.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24ee0-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="24ee0-113">-InformationAction</span></span>
<span data-ttu-id="24ee0-114">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="24ee0-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="24ee0-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="24ee0-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="24ee0-116">Vidare</span><span class="sxs-lookup"><span data-stu-id="24ee0-116">Continue</span></span>
- <span data-ttu-id="24ee0-117">Över</span><span class="sxs-lookup"><span data-stu-id="24ee0-117">Ignore</span></span>
- <span data-ttu-id="24ee0-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="24ee0-118">Inquire</span></span>
- <span data-ttu-id="24ee0-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="24ee0-119">SilentlyContinue</span></span>
- <span data-ttu-id="24ee0-120">Stanna</span><span class="sxs-lookup"><span data-stu-id="24ee0-120">Stop</span></span>
- <span data-ttu-id="24ee0-121">Avbryt</span><span class="sxs-lookup"><span data-stu-id="24ee0-121">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24ee0-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="24ee0-122">-InformationVariable</span></span>
<span data-ttu-id="24ee0-123">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="24ee0-123">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24ee0-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="24ee0-124">-Profile</span></span>
<span data-ttu-id="24ee0-125">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="24ee0-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="24ee0-126">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="24ee0-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="24ee0-127">-RoleName</span><span class="sxs-lookup"><span data-stu-id="24ee0-127">-RoleName</span></span>
<span data-ttu-id="24ee0-128">Anger namnet på den roll som du vill ange antal instanser för.</span><span class="sxs-lookup"><span data-stu-id="24ee0-128">Specifies the name of the role for which to set the number of instances.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24ee0-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="24ee0-129">-ServiceName</span></span>
<span data-ttu-id="24ee0-130">Anger namnet på Azure-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="24ee0-130">Specifies the name of the Azure service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24ee0-131">-Plats</span><span class="sxs-lookup"><span data-stu-id="24ee0-131">-Slot</span></span>
<span data-ttu-id="24ee0-132">Anger distributions miljön för den distribution som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="24ee0-132">Specifies the deployment environment of the deployment to modify.</span></span>
<span data-ttu-id="24ee0-133">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="24ee0-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="24ee0-134">Produktionsoperationsföljden</span><span class="sxs-lookup"><span data-stu-id="24ee0-134">Production</span></span>
- <span data-ttu-id="24ee0-135">Lagring</span><span class="sxs-lookup"><span data-stu-id="24ee0-135">Staging</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24ee0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24ee0-136">CommonParameters</span></span>
<span data-ttu-id="24ee0-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24ee0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24ee0-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24ee0-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24ee0-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="24ee0-139">INPUTS</span></span>

## <span data-ttu-id="24ee0-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="24ee0-140">OUTPUTS</span></span>

## <span data-ttu-id="24ee0-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="24ee0-141">NOTES</span></span>

## <span data-ttu-id="24ee0-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="24ee0-142">RELATED LINKS</span></span>

[<span data-ttu-id="24ee0-143">Get-AzureRole</span><span class="sxs-lookup"><span data-stu-id="24ee0-143">Get-AzureRole</span></span>](./Get-AzureRole.md)


