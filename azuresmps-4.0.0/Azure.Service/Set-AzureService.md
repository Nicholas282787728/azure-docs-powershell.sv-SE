---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4A920D84-0005-45A2-8229-FD9436A2CA6D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 927520466299776326229976b355444f9db6c23e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099279"
---
# <span data-ttu-id="cc4af-101">Set-AzureService</span><span class="sxs-lookup"><span data-stu-id="cc4af-101">Set-AzureService</span></span>

## <span data-ttu-id="cc4af-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cc4af-102">SYNOPSIS</span></span>
<span data-ttu-id="cc4af-103">Anger eller uppdaterar etiketten och beskrivningen för den angivna Microsoft Azure-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="cc4af-103">Sets or updates the label and description of the specified Microsoft Azure service.</span></span>

## <span data-ttu-id="cc4af-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cc4af-104">SYNTAX</span></span>

```
Set-AzureService [-ServiceName] <String> [[-Label] <String>] [[-Description] <String>]
 [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="cc4af-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cc4af-105">DESCRIPTION</span></span>
<span data-ttu-id="cc4af-106">Cmdleten **set-AzureService** tilldelar en etikett och en beskrivning till en tjänst i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="cc4af-106">The **Set-AzureService** cmdlet assigns a label and description to a service in the current subscription.</span></span>

## <span data-ttu-id="cc4af-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cc4af-107">EXAMPLES</span></span>

### <span data-ttu-id="cc4af-108">Exempel 1: uppdatera etiketten och beskrivningen för en tjänst</span><span class="sxs-lookup"><span data-stu-id="cc4af-108">Example 1: Update the label and description for a service</span></span>
```
PS C:\> C:\PS>Set-AzureService -ServiceName "MySvc1" -Label "MyTestSvc1" -Description "My service for testing out new configurations"
```

<span data-ttu-id="cc4af-109">Det här kommandot anger etiketten till "MyTestSvc1" och beskrivningen till "min tjänst för testning av nya konfigurationer" för MyTestSvc1-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="cc4af-109">This command sets the label to "MyTestSvc1" and the description to "My service for testing out new configurations" for the MyTestSvc1 service.</span></span>

## <span data-ttu-id="cc4af-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cc4af-110">PARAMETERS</span></span>

### <span data-ttu-id="cc4af-111">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="cc4af-111">-Description</span></span>
<span data-ttu-id="cc4af-112">Anger en beskrivning för Azure-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="cc4af-112">Specifies a description for the Azure service.</span></span>
<span data-ttu-id="cc4af-113">Beskrivningen kan vara upp till 1024 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="cc4af-113">The description may be up to 1024 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc4af-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="cc4af-114">-InformationAction</span></span>
<span data-ttu-id="cc4af-115">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="cc4af-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="cc4af-116">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="cc4af-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cc4af-117">Vidare</span><span class="sxs-lookup"><span data-stu-id="cc4af-117">Continue</span></span>
- <span data-ttu-id="cc4af-118">Över</span><span class="sxs-lookup"><span data-stu-id="cc4af-118">Ignore</span></span>
- <span data-ttu-id="cc4af-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="cc4af-119">Inquire</span></span>
- <span data-ttu-id="cc4af-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="cc4af-120">SilentlyContinue</span></span>
- <span data-ttu-id="cc4af-121">Stanna</span><span class="sxs-lookup"><span data-stu-id="cc4af-121">Stop</span></span>
- <span data-ttu-id="cc4af-122">Avbryt</span><span class="sxs-lookup"><span data-stu-id="cc4af-122">Suspend</span></span>

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

### <span data-ttu-id="cc4af-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="cc4af-123">-InformationVariable</span></span>
<span data-ttu-id="cc4af-124">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="cc4af-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="cc4af-125">-Etikett</span><span class="sxs-lookup"><span data-stu-id="cc4af-125">-Label</span></span>
<span data-ttu-id="cc4af-126">Anger en etikett för Azure-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="cc4af-126">Specifies a label for the Azure service.</span></span>
<span data-ttu-id="cc4af-127">Etiketten kan vara upp till 100 tecken lång.</span><span class="sxs-lookup"><span data-stu-id="cc4af-127">The label may be up to 100 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc4af-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="cc4af-128">-Profile</span></span>
<span data-ttu-id="cc4af-129">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="cc4af-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cc4af-130">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="cc4af-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cc4af-131">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="cc4af-131">-ReverseDnsFqdn</span></span>
<span data-ttu-id="cc4af-132">Anger det fullständigt kvalificerade domän namnet för omvänd DNS.</span><span class="sxs-lookup"><span data-stu-id="cc4af-132">Specifies the fully qualified domain name for reverse DNS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc4af-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="cc4af-133">-ServiceName</span></span>
<span data-ttu-id="cc4af-134">Anger namnet på den Azure-tjänst som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="cc4af-134">Specifies the name of the Azure service to update.</span></span>

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

### <span data-ttu-id="cc4af-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc4af-135">CommonParameters</span></span>
<span data-ttu-id="cc4af-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc4af-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc4af-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc4af-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc4af-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cc4af-138">INPUTS</span></span>

## <span data-ttu-id="cc4af-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cc4af-139">OUTPUTS</span></span>

### <span data-ttu-id="cc4af-140">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="cc4af-140">ManagementOperationContext</span></span>

## <span data-ttu-id="cc4af-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cc4af-141">NOTES</span></span>

## <span data-ttu-id="cc4af-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cc4af-142">RELATED LINKS</span></span>

[<span data-ttu-id="cc4af-143">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="cc4af-143">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="cc4af-144">New-AzureService</span><span class="sxs-lookup"><span data-stu-id="cc4af-144">New-AzureService</span></span>](./New-AzureService.md)


