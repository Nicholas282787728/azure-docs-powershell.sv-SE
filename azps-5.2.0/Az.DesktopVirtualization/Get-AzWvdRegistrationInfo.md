---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
ms.openlocfilehash: 33e0b68e70cb65eee4e9e3178745645aafeb9f9f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391723"
---
# <span data-ttu-id="d4095-101">Get-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="d4095-101">Get-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="d4095-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d4095-102">SYNOPSIS</span></span>
<span data-ttu-id="d4095-103">Hämta registrerings informationen för Windows Virtual Desktop.</span><span class="sxs-lookup"><span data-stu-id="d4095-103">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="d4095-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d4095-104">SYNTAX</span></span>

```
Get-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d4095-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d4095-105">DESCRIPTION</span></span>
<span data-ttu-id="d4095-106">Hämta registrerings informationen för Windows Virtual Desktop.</span><span class="sxs-lookup"><span data-stu-id="d4095-106">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="d4095-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d4095-107">EXAMPLES</span></span>

### <span data-ttu-id="d4095-108">Exempel 1: Hämta ett registrerings-token för Windows Virtual Desktop</span><span class="sxs-lookup"><span data-stu-id="d4095-108">Example 1: Get a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Get-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM None                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="d4095-109">Det här kommandot får ett Windows-registrerings-token för virtuella skriv bord i en adresspool.</span><span class="sxs-lookup"><span data-stu-id="d4095-109">This command gets a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="d4095-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d4095-110">PARAMETERS</span></span>

### <span data-ttu-id="d4095-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4095-111">-DefaultProfile</span></span>
<span data-ttu-id="d4095-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d4095-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4095-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="d4095-113">-HostPoolName</span></span>
<span data-ttu-id="d4095-114">Namn på värddator</span><span class="sxs-lookup"><span data-stu-id="d4095-114">Host Pool Name</span></span>

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

### <span data-ttu-id="d4095-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4095-115">-ResourceGroupName</span></span>
<span data-ttu-id="d4095-116">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="d4095-116">Resource Group Name</span></span>

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

### <span data-ttu-id="d4095-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4095-117">-SubscriptionId</span></span>
<span data-ttu-id="d4095-118">Abonnemangs-ID</span><span class="sxs-lookup"><span data-stu-id="d4095-118">Subscription Id</span></span>

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

### <span data-ttu-id="d4095-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4095-119">CommonParameters</span></span>
<span data-ttu-id="d4095-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4095-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4095-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4095-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4095-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d4095-122">INPUTS</span></span>

## <span data-ttu-id="d4095-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d4095-123">OUTPUTS</span></span>

### <span data-ttu-id="d4095-124">Microsoft. Azure. PowerShell. cmdletar. DesktopVirtualization. Models. Api20201019Preview. RegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="d4095-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.RegistrationInfo</span></span>

## <span data-ttu-id="d4095-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d4095-125">NOTES</span></span>

<span data-ttu-id="d4095-126">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d4095-126">ALIASES</span></span>

## <span data-ttu-id="d4095-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d4095-127">RELATED LINKS</span></span>

