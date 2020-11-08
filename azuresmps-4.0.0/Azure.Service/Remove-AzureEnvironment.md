---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 4B8B56B4-511B-45BD-9595-B47187C76E03
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5af23a3ef727aa54e8223b2d07e60c2d8dbc7b8d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099707"
---
# <span data-ttu-id="ff7d1-101">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="ff7d1-101">Remove-AzureEnvironment</span></span>

## <span data-ttu-id="ff7d1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff7d1-102">SYNOPSIS</span></span>
<span data-ttu-id="ff7d1-103">Tar bort en Azure-miljö från Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ff7d1-103">Deletes an Azure environment from Windows PowerShell.</span></span>

## <span data-ttu-id="ff7d1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff7d1-104">SYNTAX</span></span>

```
Remove-AzureEnvironment -Name <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ff7d1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff7d1-105">DESCRIPTION</span></span>
<span data-ttu-id="ff7d1-106">Cmdleten **Remove-AzureEnvironment** tar bort en Azure-miljö från din centrala profil så att Windows PowerShell inte hittar den.</span><span class="sxs-lookup"><span data-stu-id="ff7d1-106">The **Remove-AzureEnvironment** cmdlet deletes an Azure environment from your roaming profile so Windows PowerShell can't find it.</span></span>
<span data-ttu-id="ff7d1-107">Denna cmdlet tar inte bort miljön från Microsoft Azure eller ändrar den faktiska miljön på något sätt.</span><span class="sxs-lookup"><span data-stu-id="ff7d1-107">This cmdlet does not delete the environment from Microsoft Azure, or change the actual environment in any way.</span></span>

<span data-ttu-id="ff7d1-108">En Azure-miljö en oberoende distribution av Microsoft Azure, till exempel AzureCloud för globala Azure-och AzureChinaCloud för Azure som drivs av 21Vianet i Kina.</span><span class="sxs-lookup"><span data-stu-id="ff7d1-108">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="ff7d1-109">Du kan också skapa lokala Azure-miljöer med Azure Pack och WAPack cmdlets.</span><span class="sxs-lookup"><span data-stu-id="ff7d1-109">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="ff7d1-110">Mer information finns i [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ff7d1-110">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

## <span data-ttu-id="ff7d1-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff7d1-111">EXAMPLES</span></span>

### <span data-ttu-id="ff7d1-112">Exempel 1: ta bort en miljö</span><span class="sxs-lookup"><span data-stu-id="ff7d1-112">Example 1: Delete an environment</span></span>
```
PS C:\> Remove-AzureEnvironment -Name ContosoEnv
```

<span data-ttu-id="ff7d1-113">Det här kommandot tar bort ContosoEnv-miljön från Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ff7d1-113">This command deletes the ContosoEnv environment from Windows PowerShell.</span></span>

### <span data-ttu-id="ff7d1-114">Exempel 2: ta bort flera miljöer</span><span class="sxs-lookup"><span data-stu-id="ff7d1-114">Example 2: Delete multiple environments</span></span>
```
PS C:\> Get-AzureEnvironment | Where-Object EnvironmentName -like "Contoso*" | ForEach-Object {Remove-AzureEnvironment -Name $_.EnvironmentName }
```

<span data-ttu-id="ff7d1-115">Det här kommandot tar bort miljöer vars namn börjar med "contoso" från Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ff7d1-115">This command deletes environments whose names begin with "Contoso" from Windows PowerShell.</span></span>

## <span data-ttu-id="ff7d1-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff7d1-116">PARAMETERS</span></span>

### <span data-ttu-id="ff7d1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ff7d1-117">-Force</span></span>
<span data-ttu-id="ff7d1-118">Inaktiverar uppmaningen om att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="ff7d1-118">Suppresses the confirmation prompt.</span></span>

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

### <span data-ttu-id="ff7d1-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="ff7d1-119">-Name</span></span>
<span data-ttu-id="ff7d1-120">Anger namnet på den miljö som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="ff7d1-120">Specifies the name of the environment to remove.</span></span>
<span data-ttu-id="ff7d1-121">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="ff7d1-121">This parameter is required.</span></span>
<span data-ttu-id="ff7d1-122">Det här parametervärdet är Skift läges känsligt.</span><span class="sxs-lookup"><span data-stu-id="ff7d1-122">This parameter value is case-sensitive.</span></span>
<span data-ttu-id="ff7d1-123">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="ff7d1-123">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="ff7d1-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="ff7d1-124">-Profile</span></span>
<span data-ttu-id="ff7d1-125">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="ff7d1-125">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="ff7d1-126">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="ff7d1-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ff7d1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff7d1-127">CommonParameters</span></span>
<span data-ttu-id="ff7d1-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff7d1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff7d1-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff7d1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff7d1-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff7d1-130">INPUTS</span></span>

### <span data-ttu-id="ff7d1-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="ff7d1-131">None</span></span>
<span data-ttu-id="ff7d1-132">Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="ff7d1-132">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="ff7d1-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff7d1-133">OUTPUTS</span></span>

### <span data-ttu-id="ff7d1-134">Ingen eller system. Boolean</span><span class="sxs-lookup"><span data-stu-id="ff7d1-134">None or System.Boolean</span></span>
<span data-ttu-id="ff7d1-135">Om du använder parametern *Passthru* returnerar denna cmdlet ett Boolean-värde.</span><span class="sxs-lookup"><span data-stu-id="ff7d1-135">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="ff7d1-136">Annars returnerar den inte några resultat.</span><span class="sxs-lookup"><span data-stu-id="ff7d1-136">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="ff7d1-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff7d1-137">NOTES</span></span>

## <span data-ttu-id="ff7d1-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff7d1-138">RELATED LINKS</span></span>

[<span data-ttu-id="ff7d1-139">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="ff7d1-139">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="ff7d1-140">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="ff7d1-140">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="ff7d1-141">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="ff7d1-141">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


