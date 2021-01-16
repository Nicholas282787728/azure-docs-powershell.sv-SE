---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
ms.openlocfilehash: 94692e40f53026e7f554dd124e112399c949205d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400811"
---
# <span data-ttu-id="93fa0-101">New-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="93fa0-101">New-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="93fa0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="93fa0-102">SYNOPSIS</span></span>
<span data-ttu-id="93fa0-103">Skapa fjärrstyrt konto</span><span class="sxs-lookup"><span data-stu-id="93fa0-103">Create Remote Rendering Account</span></span>

## <span data-ttu-id="93fa0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="93fa0-104">SYNTAX</span></span>

```
New-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93fa0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="93fa0-105">DESCRIPTION</span></span>
<span data-ttu-id="93fa0-106">Skapa ett nytt konto för fjärrrendering i vissa abonnemang, resurs grupper och region.</span><span class="sxs-lookup"><span data-stu-id="93fa0-106">Create a new Remote Rendering Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="93fa0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="93fa0-107">EXAMPLES</span></span>

### <span data-ttu-id="93fa0-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="93fa0-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmRemoteRenderingAccount -ResourceGroup rg1 -Name example -Location centralus

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : centralus
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/RemoteRenderingAccounts/example
Name                : example
Type                : Microsoft.MixedReality/RemoteRenderingAccounts
```

<span data-ttu-id="93fa0-109">Skapa ett nytt fjärråter givnings konto "exempel" i aktuell prenumeration, resurs grupp "RG1" och Central.</span><span class="sxs-lookup"><span data-stu-id="93fa0-109">Create a new Remote Rendering Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="93fa0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="93fa0-110">PARAMETERS</span></span>

### <span data-ttu-id="93fa0-111">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="93fa0-111">-Confirm</span></span>
<span data-ttu-id="93fa0-112">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="93fa0-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93fa0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93fa0-113">-DefaultProfile</span></span>
<span data-ttu-id="93fa0-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="93fa0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93fa0-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="93fa0-115">-Location</span></span>
<span data-ttu-id="93fa0-116">Plats för fjärrrendering-konto.</span><span class="sxs-lookup"><span data-stu-id="93fa0-116">Remote Rendering Account Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93fa0-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="93fa0-117">-Name</span></span>
<span data-ttu-id="93fa0-118">Namn på fjärrrendering-konto.</span><span class="sxs-lookup"><span data-stu-id="93fa0-118">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93fa0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93fa0-119">-ResourceGroupName</span></span>
<span data-ttu-id="93fa0-120">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="93fa0-120">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93fa0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93fa0-121">-WhatIf</span></span>
<span data-ttu-id="93fa0-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="93fa0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93fa0-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="93fa0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93fa0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93fa0-124">CommonParameters</span></span>
<span data-ttu-id="93fa0-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93fa0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="93fa0-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93fa0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93fa0-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="93fa0-127">INPUTS</span></span>

### <span data-ttu-id="93fa0-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="93fa0-128">None</span></span>

## <span data-ttu-id="93fa0-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="93fa0-129">OUTPUTS</span></span>

### <span data-ttu-id="93fa0-130">Microsoft. Azure. commands. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="93fa0-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="93fa0-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="93fa0-131">NOTES</span></span>

## <span data-ttu-id="93fa0-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="93fa0-132">RELATED LINKS</span></span>
