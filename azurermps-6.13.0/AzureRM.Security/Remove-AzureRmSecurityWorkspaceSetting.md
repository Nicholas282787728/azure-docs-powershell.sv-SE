---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
ms.openlocfilehash: 1c6f6a38c1811bdda32b60d4af1707c78eb7afd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755811"
---
# <span data-ttu-id="d6d6c-101">Remove-AzureRmSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="d6d6c-101">Remove-AzureRmSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="d6d6c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d6d6c-102">SYNOPSIS</span></span>
<span data-ttu-id="d6d6c-103">Tar bort inställningen för säkerhets arbets ytan för det här abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="d6d6c-103">Deletes the security workspace setting for this subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6d6c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d6d6c-104">SYNTAX</span></span>

### <span data-ttu-id="d6d6c-105">SubscriptionLevelResource (standard)</span><span class="sxs-lookup"><span data-stu-id="d6d6c-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6d6c-106">ID</span><span class="sxs-lookup"><span data-stu-id="d6d6c-106">ResourceId</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6d6c-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="d6d6c-107">InputObject</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -InputObject <PSRemoveWorkspaceSettingInputObject> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6d6c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d6d6c-108">DESCRIPTION</span></span>
<span data-ttu-id="d6d6c-109">Tar bort inställningen för säkerhets arbets ytan för det här abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="d6d6c-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="d6d6c-110">Den här åtgärden gör att de nyligen installerade säkerhets agenterna kan rapportera till standard arbets ytan för denna susbscription.</span><span class="sxs-lookup"><span data-stu-id="d6d6c-110">This action will make the newly installed security agents to report to the default workspace of this susbscription.</span></span>

## <span data-ttu-id="d6d6c-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d6d6c-111">EXAMPLES</span></span>

### <span data-ttu-id="d6d6c-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d6d6c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="d6d6c-113">Tar bort inställningen för säkerhets arbets ytan för det här abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="d6d6c-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="d6d6c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d6d6c-114">PARAMETERS</span></span>

### <span data-ttu-id="d6d6c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6d6c-115">-DefaultProfile</span></span>
<span data-ttu-id="d6d6c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d6d6c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6d6c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6d6c-117">-InputObject</span></span>
<span data-ttu-id="d6d6c-118">Indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="d6d6c-118">Input Object.</span></span>

```yaml
Type: PSRemoveWorkspaceSettingInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6d6c-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="d6d6c-119">-Name</span></span>
<span data-ttu-id="d6d6c-120">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="d6d6c-120">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6d6c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6d6c-121">-PassThru</span></span>
<span data-ttu-id="d6d6c-122">Returnera om åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="d6d6c-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="d6d6c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6d6c-123">-ResourceId</span></span>
<span data-ttu-id="d6d6c-124">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="d6d6c-124">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6d6c-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d6d6c-125">-Confirm</span></span>
<span data-ttu-id="d6d6c-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d6d6c-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6d6c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6d6c-127">-WhatIf</span></span>
<span data-ttu-id="d6d6c-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d6d6c-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d6d6c-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d6d6c-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6d6c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6d6c-130">CommonParameters</span></span>
<span data-ttu-id="d6d6c-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6d6c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6d6c-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6d6c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6d6c-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d6d6c-133">INPUTS</span></span>

### <span data-ttu-id="d6d6c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d6d6c-134">System.String</span></span>
<span data-ttu-id="d6d6c-135">Microsoft. Azure. kommandon. Security. cmdletar. WorkspaceSettings. PSRemoveWorkspaceSettingInputObject</span><span class="sxs-lookup"><span data-stu-id="d6d6c-135">Microsoft.Azure.Commands.Security.Cmdlets.WorkspaceSettings.PSRemoveWorkspaceSettingInputObject</span></span>

## <span data-ttu-id="d6d6c-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d6d6c-136">OUTPUTS</span></span>

### <span data-ttu-id="d6d6c-137">Microsoft. Azure. commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="d6d6c-137">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="d6d6c-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d6d6c-138">NOTES</span></span>

## <span data-ttu-id="d6d6c-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d6d6c-139">RELATED LINKS</span></span>
