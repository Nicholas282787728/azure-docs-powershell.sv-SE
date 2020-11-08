---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
ms.openlocfilehash: bdef7b776d8da82a357d535ff91298a2f49e9e4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259986"
---
# <span data-ttu-id="af032-101">Remove-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="af032-101">Remove-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="af032-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af032-102">SYNOPSIS</span></span>
<span data-ttu-id="af032-103">Ta bort registrerings informationen för Windows Virtual Desktop.</span><span class="sxs-lookup"><span data-stu-id="af032-103">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="af032-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af032-104">SYNTAX</span></span>

```
Remove-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="af032-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af032-105">DESCRIPTION</span></span>
<span data-ttu-id="af032-106">Ta bort registrerings informationen för Windows Virtual Desktop.</span><span class="sxs-lookup"><span data-stu-id="af032-106">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="af032-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af032-107">EXAMPLES</span></span>

### <span data-ttu-id="af032-108">Exempel 1: ta bort ett registrerings-token för Windows Virtual Desktop</span><span class="sxs-lookup"><span data-stu-id="af032-108">Example 1: Delete a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Remove-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName
```

<span data-ttu-id="af032-109">Det här kommandot tar bort ett registrerings-token för Windows virtuella skriv bord i en adresspool.</span><span class="sxs-lookup"><span data-stu-id="af032-109">This command deletes a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="af032-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af032-110">PARAMETERS</span></span>

### <span data-ttu-id="af032-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af032-111">-DefaultProfile</span></span>
<span data-ttu-id="af032-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="af032-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af032-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="af032-113">-HostPoolName</span></span>
<span data-ttu-id="af032-114">Namn på värddator</span><span class="sxs-lookup"><span data-stu-id="af032-114">Host Pool Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af032-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af032-115">-ResourceGroupName</span></span>
<span data-ttu-id="af032-116">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="af032-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af032-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="af032-117">-SubscriptionId</span></span>
<span data-ttu-id="af032-118">hjälp för foo 1</span><span class="sxs-lookup"><span data-stu-id="af032-118">help foo 1</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af032-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="af032-119">-Confirm</span></span>
<span data-ttu-id="af032-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="af032-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af032-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af032-121">-WhatIf</span></span>
<span data-ttu-id="af032-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="af032-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af032-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="af032-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af032-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af032-124">CommonParameters</span></span>
<span data-ttu-id="af032-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af032-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af032-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af032-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af032-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af032-127">INPUTS</span></span>

## <span data-ttu-id="af032-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af032-128">OUTPUTS</span></span>

## <span data-ttu-id="af032-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af032-129">NOTES</span></span>

<span data-ttu-id="af032-130">ALIAS</span><span class="sxs-lookup"><span data-stu-id="af032-130">ALIASES</span></span>

## <span data-ttu-id="af032-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af032-131">RELATED LINKS</span></span>

