---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
ms.openlocfilehash: 09273ee53eb3e4ced7249505e73f4f9f39db5291
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269420"
---
# <span data-ttu-id="2baab-101">Set-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="2baab-101">Set-AzSecuritySetting</span></span>

## <span data-ttu-id="2baab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2baab-102">SYNOPSIS</span></span>
<span data-ttu-id="2baab-103">Uppdatera en säkerhets inställning i Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="2baab-103">Update a security setting in Azure Security Center</span></span>

## <span data-ttu-id="2baab-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2baab-104">SYNTAX</span></span>

### <span data-ttu-id="2baab-105">GeneralScope (standard)</span><span class="sxs-lookup"><span data-stu-id="2baab-105">GeneralScope (Default)</span></span>
```
Set-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2baab-106">DataExportSettingsScope</span><span class="sxs-lookup"><span data-stu-id="2baab-106">DataExportSettingsScope</span></span>
```
Set-AzSecuritySetting -SettingName <String> -SettingKind <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2baab-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="2baab-107">InputObject</span></span>
```
Set-AzSecuritySetting -InputObject <PSSecuritySetting> [-Enabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2baab-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2baab-108">DESCRIPTION</span></span>
<span data-ttu-id="2baab-109">Set-AzSecuritySetting cmdlet uppdaterar en särskild säkerhets inställning i Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="2baab-109">The Set-AzSecuritySetting cmdlet updates a specific security setting in Azure Security Center.</span></span>

## <span data-ttu-id="2baab-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2baab-110">EXAMPLES</span></span>

### <span data-ttu-id="2baab-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2baab-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS" -SettingKind "DataExportSettings" -Enabled $true

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="2baab-112">Uppdaterar en inställning för MCAS data export</span><span class="sxs-lookup"><span data-stu-id="2baab-112">Updates an MCAS data export setting</span></span>   

## <span data-ttu-id="2baab-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2baab-113">PARAMETERS</span></span>

### <span data-ttu-id="2baab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2baab-114">-DefaultProfile</span></span>
<span data-ttu-id="2baab-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2baab-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2baab-116">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="2baab-116">-Enabled</span></span>
<span data-ttu-id="2baab-117">Aktiverar inställningen.</span><span class="sxs-lookup"><span data-stu-id="2baab-117">Enables the setting.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2baab-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2baab-118">-InputObject</span></span>
<span data-ttu-id="2baab-119">Indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="2baab-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2baab-120">-SettingKind</span><span class="sxs-lookup"><span data-stu-id="2baab-120">-SettingKind</span></span>
<span data-ttu-id="2baab-121">Inställnings typ.</span><span class="sxs-lookup"><span data-stu-id="2baab-121">Setting kind.</span></span> <span data-ttu-id="2baab-122">(DataExportSettings)</span><span class="sxs-lookup"><span data-stu-id="2baab-122">(DataExportSettings)</span></span>

```yaml
Type: System.String
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2baab-123">-SettingName</span><span class="sxs-lookup"><span data-stu-id="2baab-123">-SettingName</span></span>
<span data-ttu-id="2baab-124">Ange namn.</span><span class="sxs-lookup"><span data-stu-id="2baab-124">Setting name.</span></span> <span data-ttu-id="2baab-125">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="2baab-125">(MCAS/WDATP)</span></span>

```yaml
Type: System.String
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2baab-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2baab-126">-Confirm</span></span>
<span data-ttu-id="2baab-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2baab-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2baab-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2baab-128">-WhatIf</span></span>
<span data-ttu-id="2baab-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2baab-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2baab-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2baab-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2baab-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2baab-131">CommonParameters</span></span>
<span data-ttu-id="2baab-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2baab-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2baab-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2baab-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2baab-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2baab-134">INPUTS</span></span>

### <span data-ttu-id="2baab-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2baab-135">System.String</span></span>
### <span data-ttu-id="2baab-136">Microsoft. Azure. commands. Security. Models. Settings. PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="2baab-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="2baab-137">Microsoft. Azure. commands. Security. Models. Settings. PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="2baab-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

### <span data-ttu-id="2baab-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2baab-138">System.Boolean</span></span>

## <span data-ttu-id="2baab-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2baab-139">OUTPUTS</span></span>

### <span data-ttu-id="2baab-140">Microsoft. Azure. commands. Security. Models. Settings. PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="2baab-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="2baab-141">Microsoft. Azure. commands. Security. Models. Settings. PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="2baab-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="2baab-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2baab-142">NOTES</span></span>

## <span data-ttu-id="2baab-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2baab-143">RELATED LINKS</span></span>
