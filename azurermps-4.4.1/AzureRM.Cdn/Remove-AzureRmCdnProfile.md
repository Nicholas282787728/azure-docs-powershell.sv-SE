---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
ms.openlocfilehash: f564a026359042a20e5d82e34425e98f1021422b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578447"
---
# <span data-ttu-id="a3283-101">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a3283-101">Remove-AzureRmCdnProfile</span></span>

## <span data-ttu-id="a3283-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a3283-102">SYNOPSIS</span></span>
<span data-ttu-id="a3283-103">Tar bort en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="a3283-103">Removes a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3283-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a3283-104">SYNTAX</span></span>

### <span data-ttu-id="a3283-105">Parameter uppsättning för fält parametrar</span><span class="sxs-lookup"><span data-stu-id="a3283-105">Parameter Set for fields parameters</span></span>
```
Remove-AzureRmCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3283-106">Parameter uppsättning för objekt parametrar</span><span class="sxs-lookup"><span data-stu-id="a3283-106">Parameter Set for object parameters</span></span>
```
Remove-AzureRmCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3283-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a3283-107">DESCRIPTION</span></span>
<span data-ttu-id="a3283-108">Cmdleten **Remove-AzureRmCdnProfile** tar bort en CDN-profil.</span><span class="sxs-lookup"><span data-stu-id="a3283-108">The **Remove-AzureRmCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="a3283-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a3283-109">EXAMPLES</span></span>

## <span data-ttu-id="a3283-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a3283-110">PARAMETERS</span></span>

### <span data-ttu-id="a3283-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="a3283-111">-CdnProfile</span></span>
<span data-ttu-id="a3283-112">Anger den profil som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="a3283-112">Specifies the profile that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3283-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a3283-113">-Force</span></span>
<span data-ttu-id="a3283-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a3283-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3283-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3283-115">-PassThru</span></span>
<span data-ttu-id="a3283-116">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="a3283-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a3283-117">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="a3283-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3283-118">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="a3283-118">-ProfileName</span></span>
<span data-ttu-id="a3283-119">Anger namnet på den profil som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="a3283-119">Specifies the name of the profile that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3283-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3283-120">-ResourceGroupName</span></span>
<span data-ttu-id="a3283-121">Anger namnet på den resurs grupp som profilen tillhör.</span><span class="sxs-lookup"><span data-stu-id="a3283-121">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3283-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a3283-122">-Confirm</span></span>
<span data-ttu-id="a3283-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a3283-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3283-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3283-124">-WhatIf</span></span>
<span data-ttu-id="a3283-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a3283-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3283-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a3283-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3283-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3283-127">-DefaultProfile</span></span>
<span data-ttu-id="a3283-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a3283-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3283-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3283-129">CommonParameters</span></span>
<span data-ttu-id="a3283-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3283-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3283-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3283-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3283-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a3283-132">INPUTS</span></span>

### <span data-ttu-id="a3283-133">PSProfile</span><span class="sxs-lookup"><span data-stu-id="a3283-133">PSProfile</span></span>
<span data-ttu-id="a3283-134">Parametern ' CdnProfile ' godkänner värdet av typen ' PSProfile ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="a3283-134">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="a3283-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a3283-135">OUTPUTS</span></span>

### <span data-ttu-id="a3283-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a3283-136">System.Boolean</span></span>

## <span data-ttu-id="a3283-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a3283-137">NOTES</span></span>

## <span data-ttu-id="a3283-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a3283-138">RELATED LINKS</span></span>

[<span data-ttu-id="a3283-139">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a3283-139">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="a3283-140">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a3283-140">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="a3283-141">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a3283-141">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


