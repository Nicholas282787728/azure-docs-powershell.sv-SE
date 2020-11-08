---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2CBF8DEF-954C-4D9F-B495-C2F76550BC79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35f7e8a7a08ac2793b7e4aeb8615e5fb8fc1f727
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093341"
---
# <span data-ttu-id="c3129-101">Get-AzureRoleSize</span><span class="sxs-lookup"><span data-stu-id="c3129-101">Get-AzureRoleSize</span></span>

## <span data-ttu-id="c3129-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3129-102">SYNOPSIS</span></span>
<span data-ttu-id="c3129-103">Hämtar information om roll storlek för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c3129-103">Gets the role size information for the current subscription.</span></span>

## <span data-ttu-id="c3129-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3129-104">SYNTAX</span></span>

```
Get-AzureRoleSize [[-InstanceSize] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c3129-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3129-105">DESCRIPTION</span></span>
<span data-ttu-id="c3129-106">Cmdleten **Get-AzureRoleSize** hämtar information om roll storlek för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c3129-106">The **Get-AzureRoleSize** cmdlet gets the role size information for the current subscription.</span></span>

## <span data-ttu-id="c3129-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3129-107">EXAMPLES</span></span>

### <span data-ttu-id="c3129-108">Exempel 1: Hämta information om roll storlek</span><span class="sxs-lookup"><span data-stu-id="c3129-108">Example 1: Get role size information</span></span>
```
PS C:\> Get-AzureRoleSize

          InstanceSize               : A6
          RoleSizeLabel              :
          Cores                      : 4
          MemoryInMb                 : 28672
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded

          InstanceSize               : A7
          RoleSizeLabel              :
          Cores                      : 8
          MemoryInMb                 : 57344
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded
```

<span data-ttu-id="c3129-109">Det här kommandot hämtar information om roll storlek för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c3129-109">This command gets role size information for the current subscription.</span></span>

### <span data-ttu-id="c3129-110">Exempel 2: Hämta information om roll storlek och ange namnet på roll storleken</span><span class="sxs-lookup"><span data-stu-id="c3129-110">Example 2: Get role size information and specify the role size name</span></span>
```
PS C:\> Get-AzureRoleSize -InstanceSize A7

          InstanceSize               : A7
          RoleSizeLabel              :
          Cores                      : 8
          MemoryInMb                 : 57344
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded
```

<span data-ttu-id="c3129-111">Det här kommandot hämtar information om roll storlek för den angivna roll storleken.</span><span class="sxs-lookup"><span data-stu-id="c3129-111">This command gets role size information for the specified role size.</span></span>

### <span data-ttu-id="c3129-112">Exempel 3: Hämta information om roll storlek för alla virtuella datorer i alla Azure-tjänster</span><span class="sxs-lookup"><span data-stu-id="c3129-112">Example 3: Get role size information for all virtual machines in all of the Azure services</span></span>
```
PS C:\> Get-AzureService | Get-AzureVM | Get-AzureRoleSize
```

<span data-ttu-id="c3129-113">Det här kommandot hämtar information om roll storlek för alla virtuella datorer i alla Azure-tjänster.</span><span class="sxs-lookup"><span data-stu-id="c3129-113">This command gets role size information for all virtual machines in all of the Azure services.</span></span>

## <span data-ttu-id="c3129-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3129-114">PARAMETERS</span></span>

### <span data-ttu-id="c3129-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c3129-115">-InformationAction</span></span>
<span data-ttu-id="c3129-116">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="c3129-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c3129-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c3129-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c3129-118">Vidare</span><span class="sxs-lookup"><span data-stu-id="c3129-118">Continue</span></span>
- <span data-ttu-id="c3129-119">Över</span><span class="sxs-lookup"><span data-stu-id="c3129-119">Ignore</span></span>
- <span data-ttu-id="c3129-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="c3129-120">Inquire</span></span>
- <span data-ttu-id="c3129-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c3129-121">SilentlyContinue</span></span>
- <span data-ttu-id="c3129-122">Stanna</span><span class="sxs-lookup"><span data-stu-id="c3129-122">Stop</span></span>
- <span data-ttu-id="c3129-123">Avbryt</span><span class="sxs-lookup"><span data-stu-id="c3129-123">Suspend</span></span>

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

### <span data-ttu-id="c3129-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c3129-124">-InformationVariable</span></span>
<span data-ttu-id="c3129-125">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="c3129-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c3129-126">-InstanceSize</span><span class="sxs-lookup"><span data-stu-id="c3129-126">-InstanceSize</span></span>
<span data-ttu-id="c3129-127">Anger namnet på roll storleken, till exempel: ExtraSmall, Small, Large, ExtraLarge, A5, A6, A7.</span><span class="sxs-lookup"><span data-stu-id="c3129-127">Specifies the role size name, for example: ExtraSmall, Small, Large, ExtraLarge, A5, A6, A7.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3129-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="c3129-128">-Profile</span></span>
<span data-ttu-id="c3129-129">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="c3129-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c3129-130">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="c3129-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c3129-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3129-131">CommonParameters</span></span>
<span data-ttu-id="c3129-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3129-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3129-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3129-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3129-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3129-134">INPUTS</span></span>

## <span data-ttu-id="c3129-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3129-135">OUTPUTS</span></span>

## <span data-ttu-id="c3129-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3129-136">NOTES</span></span>

## <span data-ttu-id="c3129-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3129-137">RELATED LINKS</span></span>

[<span data-ttu-id="c3129-138">Get-AzureRole</span><span class="sxs-lookup"><span data-stu-id="c3129-138">Get-AzureRole</span></span>](./Get-AzureRole.md)

[<span data-ttu-id="c3129-139">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="c3129-139">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="c3129-140">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="c3129-140">Get-AzureVM</span></span>](./Get-AzureVM.md)


