---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
ms.openlocfilehash: 86ffd1038d834d20837b1f6a6087176e562c8844
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320019"
---
# <span data-ttu-id="4c3c8-101">New-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="4c3c8-101">New-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="4c3c8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4c3c8-102">SYNOPSIS</span></span>
<span data-ttu-id="4c3c8-103">Skapa registrerings information för Windows Virtual Desktop.</span><span class="sxs-lookup"><span data-stu-id="4c3c8-103">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="4c3c8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4c3c8-104">SYNTAX</span></span>

```
New-AzWvdRegistrationInfo -ExpirationTime <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4c3c8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4c3c8-105">DESCRIPTION</span></span>
<span data-ttu-id="4c3c8-106">Skapa registrerings information för Windows Virtual Desktop.</span><span class="sxs-lookup"><span data-stu-id="4c3c8-106">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="4c3c8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4c3c8-107">EXAMPLES</span></span>

### <span data-ttu-id="4c3c8-108">Exempel 1: skapa ett registrerings-token för ett virtuellt skriv bord i Windows</span><span class="sxs-lookup"><span data-stu-id="4c3c8-108">Example 1: Create a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> New-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ'))

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM Update                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="4c3c8-109">Det här kommandot skapar ett registrerings-token för Windows virtuella skriv bord i en adresspool.</span><span class="sxs-lookup"><span data-stu-id="4c3c8-109">This command creates a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="4c3c8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4c3c8-110">PARAMETERS</span></span>

### <span data-ttu-id="4c3c8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c3c8-111">-DefaultProfile</span></span>
<span data-ttu-id="4c3c8-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4c3c8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c3c8-113">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="4c3c8-113">-ExpirationTime</span></span>
<span data-ttu-id="4c3c8-114">Förfallo tid</span><span class="sxs-lookup"><span data-stu-id="4c3c8-114">Expiration Time</span></span>

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

### <span data-ttu-id="4c3c8-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="4c3c8-115">-HostPoolName</span></span>
<span data-ttu-id="4c3c8-116">Namn på värddator</span><span class="sxs-lookup"><span data-stu-id="4c3c8-116">Host Pool Name</span></span>

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

### <span data-ttu-id="4c3c8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c3c8-117">-ResourceGroupName</span></span>
<span data-ttu-id="4c3c8-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="4c3c8-118">Resource Group Name</span></span>

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

### <span data-ttu-id="4c3c8-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4c3c8-119">-SubscriptionId</span></span>
<span data-ttu-id="4c3c8-120">Abonnemangs-ID</span><span class="sxs-lookup"><span data-stu-id="4c3c8-120">Subscription Id</span></span>

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

### <span data-ttu-id="4c3c8-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4c3c8-121">-Confirm</span></span>
<span data-ttu-id="4c3c8-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4c3c8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c3c8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c3c8-123">-WhatIf</span></span>
<span data-ttu-id="4c3c8-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4c3c8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c3c8-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4c3c8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c3c8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c3c8-126">CommonParameters</span></span>
<span data-ttu-id="4c3c8-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c3c8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c3c8-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c3c8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c3c8-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4c3c8-129">INPUTS</span></span>

## <span data-ttu-id="4c3c8-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4c3c8-130">OUTPUTS</span></span>

### <span data-ttu-id="4c3c8-131">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20191210Preview. IRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="4c3c8-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IRegistrationInfo</span></span>

## <span data-ttu-id="4c3c8-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4c3c8-132">NOTES</span></span>

<span data-ttu-id="4c3c8-133">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4c3c8-133">ALIASES</span></span>

## <span data-ttu-id="4c3c8-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4c3c8-134">RELATED LINKS</span></span>

