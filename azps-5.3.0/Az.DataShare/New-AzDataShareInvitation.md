---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
ms.openlocfilehash: ea042cb0db8fcb1995a935086d188efbb6c0647f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420627"
---
# <span data-ttu-id="b77df-101">New-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="b77df-101">New-AzDataShareInvitation</span></span>

## <span data-ttu-id="b77df-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b77df-102">SYNOPSIS</span></span>
<span data-ttu-id="b77df-103">Skapar en inbjudan till dela.</span><span class="sxs-lookup"><span data-stu-id="b77df-103">Creates an invitation for share.</span></span>

## <span data-ttu-id="b77df-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b77df-104">SYNTAX</span></span>

### <span data-ttu-id="b77df-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b77df-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareInvitation [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b77df-106">ByInvitationEmailParameterSet</span><span class="sxs-lookup"><span data-stu-id="b77df-106">ByInvitationEmailParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetEmail <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b77df-107">ByInvitationTenantParameterSet</span><span class="sxs-lookup"><span data-stu-id="b77df-107">ByInvitationTenantParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetObjectId <String> -TargetTenantId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b77df-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b77df-108">DESCRIPTION</span></span>
<span data-ttu-id="b77df-109">Cmdleten **New-AzDataShareInvitation** skickar en inbjudan till mål konsumenten med information om leverantörs resursen.</span><span class="sxs-lookup"><span data-stu-id="b77df-109">The **New-AzDataShareInvitation** cmdlet sends an invitation to the target consumer with information about the provider share.</span></span> 

## <span data-ttu-id="b77df-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b77df-110">EXAMPLES</span></span>

### <span data-ttu-id="b77df-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b77df-111">Example 1</span></span>
```
PS C:\> New-AzDataShareInvitation -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsInvitation" -TargetEmail "adstest@microsoft.com"
InvitationId     : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus : Pending
Sender           : adsprovider@microsoft.com
SentAt           : 7/8/2019 10:47:10 PM
TargetEmail      : adstest@microsoft.com
TargetObjectId   :
TargetTenantId   :
Id               : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/        providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/invitations/AdsInvitation
Name             : AdsInvitation
Type             : Microsoft.DataShare/Invitations
```

<span data-ttu-id="b77df-112">Det här kommandot skapar en inbjudan-AdsInvitation för dela AdsShare och skickar den till en mål-e-postadress adstest@microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="b77df-112">This command creates an invitation AdsInvitation for share AdsShare and sends it to target email adstest@microsoft.com.</span></span>

## <span data-ttu-id="b77df-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b77df-113">PARAMETERS</span></span>

### <span data-ttu-id="b77df-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b77df-114">-AccountName</span></span>
<span data-ttu-id="b77df-115">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="b77df-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b77df-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b77df-116">-DefaultProfile</span></span>
<span data-ttu-id="b77df-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b77df-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b77df-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="b77df-118">-Name</span></span>
<span data-ttu-id="b77df-119">Namn på Azure Data-delningsinbjudan</span><span class="sxs-lookup"><span data-stu-id="b77df-119">Azure data share invitation name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b77df-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b77df-120">-ResourceGroupName</span></span>
<span data-ttu-id="b77df-121">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="b77df-121">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b77df-122">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b77df-122">-ShareName</span></span>
<span data-ttu-id="b77df-123">Azure Data Share-namn</span><span class="sxs-lookup"><span data-stu-id="b77df-123">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b77df-124">-TargetEmail</span><span class="sxs-lookup"><span data-stu-id="b77df-124">-TargetEmail</span></span>
<span data-ttu-id="b77df-125">Mål-e-postadress</span><span class="sxs-lookup"><span data-stu-id="b77df-125">Target email id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b77df-126">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="b77df-126">-TargetObjectId</span></span>
<span data-ttu-id="b77df-127">Målprogram-ID</span><span class="sxs-lookup"><span data-stu-id="b77df-127">Target object id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b77df-128">-TargetTenantId</span><span class="sxs-lookup"><span data-stu-id="b77df-128">-TargetTenantId</span></span>
<span data-ttu-id="b77df-129">Mål klient organisationens ID</span><span class="sxs-lookup"><span data-stu-id="b77df-129">Target tenant id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b77df-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b77df-130">-Confirm</span></span>
<span data-ttu-id="b77df-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b77df-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b77df-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b77df-132">-WhatIf</span></span>
<span data-ttu-id="b77df-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b77df-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b77df-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b77df-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b77df-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b77df-135">CommonParameters</span></span>
<span data-ttu-id="b77df-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b77df-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b77df-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b77df-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b77df-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b77df-138">INPUTS</span></span>

### <span data-ttu-id="b77df-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="b77df-139">None</span></span>

## <span data-ttu-id="b77df-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b77df-140">OUTPUTS</span></span>

### <span data-ttu-id="b77df-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="b77df-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="b77df-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b77df-142">NOTES</span></span>

## <span data-ttu-id="b77df-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b77df-143">RELATED LINKS</span></span>
