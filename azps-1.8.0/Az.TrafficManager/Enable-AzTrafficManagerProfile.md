---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
ms.openlocfilehash: 475346fa7c446c1a6faede83a2f4e487197e674e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746132"
---
# <span data-ttu-id="43c0f-101">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="43c0f-101">Enable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="43c0f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="43c0f-102">SYNOPSIS</span></span>
<span data-ttu-id="43c0f-103">Aktiverar en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="43c0f-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="43c0f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="43c0f-104">SYNTAX</span></span>

### <span data-ttu-id="43c0f-105">Fält</span><span class="sxs-lookup"><span data-stu-id="43c0f-105">Fields</span></span>
```
Enable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43c0f-106">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="43c0f-106">Object</span></span>
```
Enable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43c0f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="43c0f-107">DESCRIPTION</span></span>
<span data-ttu-id="43c0f-108">Cmdleten **Enable-AzTrafficManagerProfile** aktiverar en Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="43c0f-108">The **Enable-AzTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="43c0f-109">Du kan ange profil objekt med hjälp av pipeline eller som ett parameter värde.</span><span class="sxs-lookup"><span data-stu-id="43c0f-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="43c0f-110">Alternativt kan du ange profilen med hjälp av parametrarna *Name* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="43c0f-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="43c0f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="43c0f-111">EXAMPLES</span></span>

### <span data-ttu-id="43c0f-112">Exempel 1: Aktivera en profil som anges med namn</span><span class="sxs-lookup"><span data-stu-id="43c0f-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="43c0f-113">Det här kommandot aktiverar profilen med namnet ContosoProfile i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="43c0f-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="43c0f-114">Exempel 2: Aktivera en profil med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="43c0f-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerProfile
```

<span data-ttu-id="43c0f-115">Det här kommandot får profilen med namnet ContosoProfile i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="43c0f-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="43c0f-116">Då överförs den profilen till cmdlet **Enable-AzTrafficManagerProfile** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="43c0f-116">The command then passes that profile to the **Enable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="43c0f-117">Denna cmdlet aktiverar den profilen.</span><span class="sxs-lookup"><span data-stu-id="43c0f-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="43c0f-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="43c0f-118">PARAMETERS</span></span>

### <span data-ttu-id="43c0f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43c0f-119">-DefaultProfile</span></span>
<span data-ttu-id="43c0f-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="43c0f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43c0f-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="43c0f-121">-Name</span></span>
<span data-ttu-id="43c0f-122">Anger namnet på den Traffic Manager-profil som denna cmdlet aktiverar.</span><span class="sxs-lookup"><span data-stu-id="43c0f-122">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43c0f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43c0f-123">-ResourceGroupName</span></span>
<span data-ttu-id="43c0f-124">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="43c0f-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="43c0f-125">Denna cmdlet aktiverar en Traffic Manager-profil i gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="43c0f-125">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43c0f-126">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="43c0f-126">-TrafficManagerProfile</span></span>
<span data-ttu-id="43c0f-127">Anger ett **TrafficManagerProfile** -objekt som ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="43c0f-127">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="43c0f-128">För att hämta ett **TrafficManagerProfile** -objekt, Använd cmdleten Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="43c0f-128">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43c0f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43c0f-129">CommonParameters</span></span>
<span data-ttu-id="43c0f-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43c0f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43c0f-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43c0f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43c0f-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="43c0f-132">INPUTS</span></span>

### <span data-ttu-id="43c0f-133">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="43c0f-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="43c0f-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="43c0f-134">OUTPUTS</span></span>

### <span data-ttu-id="43c0f-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="43c0f-135">System.Boolean</span></span>

## <span data-ttu-id="43c0f-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="43c0f-136">NOTES</span></span>

## <span data-ttu-id="43c0f-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="43c0f-137">RELATED LINKS</span></span>

[<span data-ttu-id="43c0f-138">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="43c0f-138">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="43c0f-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="43c0f-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="43c0f-140">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="43c0f-140">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="43c0f-141">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="43c0f-141">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="43c0f-142">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="43c0f-142">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


