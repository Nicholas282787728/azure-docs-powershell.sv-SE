---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
ms.openlocfilehash: 0f82c80e9f06abd5a2189bbee665de58ee6a3528
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320047"
---
# <span data-ttu-id="a0576-101">Get-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="a0576-101">Get-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="a0576-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a0576-102">SYNOPSIS</span></span>
<span data-ttu-id="a0576-103">Hämta registrerings informationen för Windows Virtual Desktop.</span><span class="sxs-lookup"><span data-stu-id="a0576-103">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="a0576-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a0576-104">SYNTAX</span></span>

```
Get-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a0576-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a0576-105">DESCRIPTION</span></span>
<span data-ttu-id="a0576-106">Hämta registrerings informationen för Windows Virtual Desktop.</span><span class="sxs-lookup"><span data-stu-id="a0576-106">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="a0576-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a0576-107">EXAMPLES</span></span>

### <span data-ttu-id="a0576-108">Exempel 1: Hämta ett registrerings-token för Windows Virtual Desktop</span><span class="sxs-lookup"><span data-stu-id="a0576-108">Example 1: Get a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Get-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM None                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="a0576-109">Det här kommandot får ett Windows-registrerings-token för virtuella skriv bord i en adresspool.</span><span class="sxs-lookup"><span data-stu-id="a0576-109">This command gets a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="a0576-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a0576-110">PARAMETERS</span></span>

### <span data-ttu-id="a0576-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0576-111">-DefaultProfile</span></span>
<span data-ttu-id="a0576-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a0576-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0576-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="a0576-113">-HostPoolName</span></span>
<span data-ttu-id="a0576-114">Namn på värddator</span><span class="sxs-lookup"><span data-stu-id="a0576-114">Host Pool Name</span></span>

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

### <span data-ttu-id="a0576-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0576-115">-ResourceGroupName</span></span>
<span data-ttu-id="a0576-116">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="a0576-116">Resource Group Name</span></span>

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

### <span data-ttu-id="a0576-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a0576-117">-SubscriptionId</span></span>
<span data-ttu-id="a0576-118">Abonnemangs-ID</span><span class="sxs-lookup"><span data-stu-id="a0576-118">Subscription Id</span></span>

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

### <span data-ttu-id="a0576-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0576-119">CommonParameters</span></span>
<span data-ttu-id="a0576-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0576-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0576-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0576-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0576-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a0576-122">INPUTS</span></span>

## <span data-ttu-id="a0576-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a0576-123">OUTPUTS</span></span>

### <span data-ttu-id="a0576-124">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20191210Preview. RegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="a0576-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.RegistrationInfo</span></span>

## <span data-ttu-id="a0576-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a0576-125">NOTES</span></span>

<span data-ttu-id="a0576-126">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a0576-126">ALIASES</span></span>

## <span data-ttu-id="a0576-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a0576-127">RELATED LINKS</span></span>

