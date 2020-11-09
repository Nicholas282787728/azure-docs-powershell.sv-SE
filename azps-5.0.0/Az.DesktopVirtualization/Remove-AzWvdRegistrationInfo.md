---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
ms.openlocfilehash: bdef7b776d8da82a357d535ff91298a2f49e9e4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319996"
---
# <span data-ttu-id="6c2ee-101">Remove-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="6c2ee-101">Remove-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="6c2ee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6c2ee-102">SYNOPSIS</span></span>
<span data-ttu-id="6c2ee-103">Ta bort registrerings informationen för Windows Virtual Desktop.</span><span class="sxs-lookup"><span data-stu-id="6c2ee-103">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="6c2ee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6c2ee-104">SYNTAX</span></span>

```
Remove-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6c2ee-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6c2ee-105">DESCRIPTION</span></span>
<span data-ttu-id="6c2ee-106">Ta bort registrerings informationen för Windows Virtual Desktop.</span><span class="sxs-lookup"><span data-stu-id="6c2ee-106">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="6c2ee-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6c2ee-107">EXAMPLES</span></span>

### <span data-ttu-id="6c2ee-108">Exempel 1: ta bort ett registrerings-token för Windows Virtual Desktop</span><span class="sxs-lookup"><span data-stu-id="6c2ee-108">Example 1: Delete a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Remove-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName
```

<span data-ttu-id="6c2ee-109">Det här kommandot tar bort ett registrerings-token för Windows virtuella skriv bord i en adresspool.</span><span class="sxs-lookup"><span data-stu-id="6c2ee-109">This command deletes a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="6c2ee-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6c2ee-110">PARAMETERS</span></span>

### <span data-ttu-id="6c2ee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c2ee-111">-DefaultProfile</span></span>
<span data-ttu-id="6c2ee-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6c2ee-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c2ee-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="6c2ee-113">-HostPoolName</span></span>
<span data-ttu-id="6c2ee-114">Namn på värddator</span><span class="sxs-lookup"><span data-stu-id="6c2ee-114">Host Pool Name</span></span>

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

### <span data-ttu-id="6c2ee-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c2ee-115">-ResourceGroupName</span></span>
<span data-ttu-id="6c2ee-116">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="6c2ee-116">Resource Group Name</span></span>

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

### <span data-ttu-id="6c2ee-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6c2ee-117">-SubscriptionId</span></span>
<span data-ttu-id="6c2ee-118">hjälp för foo 1</span><span class="sxs-lookup"><span data-stu-id="6c2ee-118">help foo 1</span></span>

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

### <span data-ttu-id="6c2ee-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6c2ee-119">-Confirm</span></span>
<span data-ttu-id="6c2ee-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6c2ee-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c2ee-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c2ee-121">-WhatIf</span></span>
<span data-ttu-id="6c2ee-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6c2ee-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c2ee-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6c2ee-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c2ee-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c2ee-124">CommonParameters</span></span>
<span data-ttu-id="6c2ee-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c2ee-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c2ee-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c2ee-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c2ee-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6c2ee-127">INPUTS</span></span>

## <span data-ttu-id="6c2ee-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6c2ee-128">OUTPUTS</span></span>

## <span data-ttu-id="6c2ee-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6c2ee-129">NOTES</span></span>

<span data-ttu-id="6c2ee-130">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6c2ee-130">ALIASES</span></span>

## <span data-ttu-id="6c2ee-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6c2ee-131">RELATED LINKS</span></span>

