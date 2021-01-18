---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
ms.openlocfilehash: bfcbaa723dc2d06d74ba4d515affd2f19a51ec3e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523777"
---
# <span data-ttu-id="2cf56-101">Remove-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="2cf56-101">Remove-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="2cf56-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2cf56-102">SYNOPSIS</span></span>
<span data-ttu-id="2cf56-103">Ta bort fjärrstyrning</span><span class="sxs-lookup"><span data-stu-id="2cf56-103">Delete Remote Rendering Account</span></span>

## <span data-ttu-id="2cf56-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2cf56-104">SYNTAX</span></span>

### <span data-ttu-id="2cf56-105">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2cf56-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cf56-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cf56-106">ResourceIdParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cf56-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cf56-107">PipelineParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -InputObject <PSRemoteRenderingAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cf56-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2cf56-108">DESCRIPTION</span></span>
<span data-ttu-id="2cf56-109">Ta bort angivet fjärrrendering-konto från vissa abonnemang och resurs grupper.</span><span class="sxs-lookup"><span data-stu-id="2cf56-109">Delete specified Remote Rendering Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="2cf56-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2cf56-110">EXAMPLES</span></span>

### <span data-ttu-id="2cf56-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2cf56-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="2cf56-112">Ta bort fjär åter givnings konto "exempel" från aktuell prenumeration och resurs grupp "RG1".</span><span class="sxs-lookup"><span data-stu-id="2cf56-112">Delete Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="2cf56-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2cf56-113">PARAMETERS</span></span>

### <span data-ttu-id="2cf56-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2cf56-114">-Confirm</span></span>
<span data-ttu-id="2cf56-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2cf56-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cf56-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cf56-116">-DefaultProfile</span></span>
<span data-ttu-id="2cf56-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2cf56-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cf56-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2cf56-118">-InputObject</span></span>
<span data-ttu-id="2cf56-119">Anpassade domän objekt.</span><span class="sxs-lookup"><span data-stu-id="2cf56-119">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cf56-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="2cf56-120">-Name</span></span>
<span data-ttu-id="2cf56-121">Namn på fjärrrendering-konto.</span><span class="sxs-lookup"><span data-stu-id="2cf56-121">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cf56-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2cf56-122">-PassThru</span></span>
<span data-ttu-id="2cf56-123">Returnera objekt om det anges.</span><span class="sxs-lookup"><span data-stu-id="2cf56-123">Return object if specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cf56-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cf56-124">-ResourceGroupName</span></span>
<span data-ttu-id="2cf56-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="2cf56-125">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cf56-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2cf56-126">-ResourceId</span></span>
<span data-ttu-id="2cf56-127">Resurs-ID för fjärrstyrt konto.</span><span class="sxs-lookup"><span data-stu-id="2cf56-127">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cf56-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cf56-128">-WhatIf</span></span>
<span data-ttu-id="2cf56-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2cf56-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cf56-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2cf56-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cf56-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cf56-131">CommonParameters</span></span>
<span data-ttu-id="2cf56-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cf56-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2cf56-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cf56-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cf56-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2cf56-134">INPUTS</span></span>

### <span data-ttu-id="2cf56-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2cf56-135">System.String</span></span>

### <span data-ttu-id="2cf56-136">Microsoft. Azure. commands. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="2cf56-136">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

### <span data-ttu-id="2cf56-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2cf56-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2cf56-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2cf56-138">OUTPUTS</span></span>

### <span data-ttu-id="2cf56-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2cf56-139">System.Boolean</span></span>

## <span data-ttu-id="2cf56-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2cf56-140">NOTES</span></span>

## <span data-ttu-id="2cf56-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2cf56-141">RELATED LINKS</span></span>
