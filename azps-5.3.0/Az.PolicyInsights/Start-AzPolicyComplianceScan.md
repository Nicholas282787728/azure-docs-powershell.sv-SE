---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicycompliancescan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
ms.openlocfilehash: 61022603ad34c345274328d47767e90580e54d6b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527315"
---
# <span data-ttu-id="6ea2e-101">Start-AzPolicyComplianceScan</span><span class="sxs-lookup"><span data-stu-id="6ea2e-101">Start-AzPolicyComplianceScan</span></span>

## <span data-ttu-id="6ea2e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6ea2e-102">SYNOPSIS</span></span>
<span data-ttu-id="6ea2e-103">Utlöser utvärdering av en policy för alla resurser i en prenumeration eller resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="6ea2e-103">Triggers a policy compliance evaluation for all resources in a subscription or resource group.</span></span>

## <span data-ttu-id="6ea2e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6ea2e-104">SYNTAX</span></span>

```
Start-AzPolicyComplianceScan [-ResourceGroupName <String>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ea2e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6ea2e-105">DESCRIPTION</span></span>
<span data-ttu-id="6ea2e-106">Cmdleten **Start-AzPolicyComplianceScan** startar en utvärdering av efterlevnadsprincip för en prenumeration eller resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="6ea2e-106">The **Start-AzPolicyComplianceScan** cmdlet starts a policy compliance evaluation for a subscription or resource group.</span></span> <span data-ttu-id="6ea2e-107">Alla resurser inom det scopet får sin efterlevnad för alla tilldelade principer.</span><span class="sxs-lookup"><span data-stu-id="6ea2e-107">All resources within that scope will have their compliance state evaluated against all assigned policies.</span></span>

## <span data-ttu-id="6ea2e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6ea2e-108">EXAMPLES</span></span>

### <span data-ttu-id="6ea2e-109">Exempel 1: starta en sökning efter en efterföljande prenumeration</span><span class="sxs-lookup"><span data-stu-id="6ea2e-109">Example 1: Start a compliance scan at subscription scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan
```

<span data-ttu-id="6ea2e-110">Det här kommandot startar en utvärdering av en policy för den aktiva prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="6ea2e-110">This command starts a policy compliance evaluation for the active subscription.</span></span>

### <span data-ttu-id="6ea2e-111">Exempel 2: starta en kompatibilitetskontroll i resurs gruppens omfattning</span><span class="sxs-lookup"><span data-stu-id="6ea2e-111">Example 2: Start a compliance scan at resource group scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan -ResourceGroupName "myRG"
```

<span data-ttu-id="6ea2e-112">Det här kommandot startar utvärderingen av en efterlevnadsprincip för resurs gruppen "myRG" i den aktiva prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="6ea2e-112">This command starts a policy compliance evaluation for the "myRG" resource group in the active subscription.</span></span>

### <span data-ttu-id="6ea2e-113">Exempel 3: starta en kompatibilitetskontroll för genomsökning och vänta tills den är klar i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6ea2e-113">Example 3: Start a compliance scan and wait for it to complete in the background</span></span>
```
PS C:\> $job = Start-AzPolicyComplianceScan -AsJob
PS C:\> $job | Wait-Job
```

<span data-ttu-id="6ea2e-114">Det här kommandot startar en utvärdering av en policy för den aktiva prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="6ea2e-114">This command starts a policy compliance evaluation for the active subscription.</span></span> <span data-ttu-id="6ea2e-115">Genomsökningen kommer att genomföras.</span><span class="sxs-lookup"><span data-stu-id="6ea2e-115">It will wait for the scan to complete.</span></span>

## <span data-ttu-id="6ea2e-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6ea2e-116">PARAMETERS</span></span>

### <span data-ttu-id="6ea2e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ea2e-117">-AsJob</span></span>
<span data-ttu-id="6ea2e-118">Kör cmdleten i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="6ea2e-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="6ea2e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ea2e-119">-DefaultProfile</span></span>
<span data-ttu-id="6ea2e-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6ea2e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ea2e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ea2e-121">-PassThru</span></span>
<span data-ttu-id="6ea2e-122">Returnera SANT om kommandot har slutförts.</span><span class="sxs-lookup"><span data-stu-id="6ea2e-122">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="6ea2e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ea2e-123">-ResourceGroupName</span></span>
<span data-ttu-id="6ea2e-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="6ea2e-124">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ea2e-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6ea2e-125">-Confirm</span></span>
<span data-ttu-id="6ea2e-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6ea2e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ea2e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ea2e-127">-WhatIf</span></span>
<span data-ttu-id="6ea2e-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6ea2e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ea2e-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6ea2e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ea2e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ea2e-130">CommonParameters</span></span>
<span data-ttu-id="6ea2e-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ea2e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ea2e-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ea2e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ea2e-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6ea2e-133">INPUTS</span></span>

### <span data-ttu-id="6ea2e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6ea2e-134">System.String</span></span>

## <span data-ttu-id="6ea2e-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6ea2e-135">OUTPUTS</span></span>

### <span data-ttu-id="6ea2e-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6ea2e-136">System.Boolean</span></span>

## <span data-ttu-id="6ea2e-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6ea2e-137">NOTES</span></span>

## <span data-ttu-id="6ea2e-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6ea2e-138">RELATED LINKS</span></span>
