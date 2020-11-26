---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: e9397a2a62ebaa4d26e0d36aaad3fbe03bad137e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103176"
---
# <span data-ttu-id="ee89f-101">Get-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="ee89f-101">Get-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="ee89f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ee89f-102">SYNOPSIS</span></span>
<span data-ttu-id="ee89f-103">Skaffa nycklar för fjärrstyrning</span><span class="sxs-lookup"><span data-stu-id="ee89f-103">Get keys of Remote Rendering Account</span></span>

## <span data-ttu-id="ee89f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ee89f-104">SYNTAX</span></span>

### <span data-ttu-id="ee89f-105">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ee89f-105">DefaultParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee89f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee89f-106">ResourceIdParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee89f-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee89f-107">PipelineParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee89f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ee89f-108">DESCRIPTION</span></span>
<span data-ttu-id="ee89f-109">Skaffa utvecklings nycklar för fjärråter givnings konto.</span><span class="sxs-lookup"><span data-stu-id="ee89f-109">Get developer keys of Remote Rendering Account.</span></span>

## <span data-ttu-id="ee89f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ee89f-110">EXAMPLES</span></span>

### <span data-ttu-id="ee89f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ee89f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="ee89f-112">Skaffa utvecklings nycklar för fjärråter givnings konto "exempel" från aktuell prenumeration och resurs grupp "RG1".</span><span class="sxs-lookup"><span data-stu-id="ee89f-112">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="ee89f-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ee89f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | Get-AzRemoteRenderingAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="ee89f-114">Skaffa utvecklings nycklar för fjärråter givnings konto "exempel" från aktuell prenumeration och resurs grupp "RG1" med rör.</span><span class="sxs-lookup"><span data-stu-id="ee89f-114">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="ee89f-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ee89f-115">PARAMETERS</span></span>

### <span data-ttu-id="ee89f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee89f-116">-DefaultProfile</span></span>
<span data-ttu-id="ee89f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ee89f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee89f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee89f-118">-InputObject</span></span>
<span data-ttu-id="ee89f-119">Anpassade domän objekt.</span><span class="sxs-lookup"><span data-stu-id="ee89f-119">The custom domain object.</span></span>

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

### <span data-ttu-id="ee89f-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="ee89f-120">-Name</span></span>
<span data-ttu-id="ee89f-121">Namn på fjärrrendering-konto.</span><span class="sxs-lookup"><span data-stu-id="ee89f-121">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="ee89f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee89f-122">-ResourceGroupName</span></span>
<span data-ttu-id="ee89f-123">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="ee89f-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="ee89f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee89f-124">-ResourceId</span></span>
<span data-ttu-id="ee89f-125">Resurs-ID för fjärrstyrt konto.</span><span class="sxs-lookup"><span data-stu-id="ee89f-125">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="ee89f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee89f-126">CommonParameters</span></span>
<span data-ttu-id="ee89f-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee89f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ee89f-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee89f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee89f-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ee89f-129">INPUTS</span></span>

### <span data-ttu-id="ee89f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ee89f-130">System.String</span></span>

### <span data-ttu-id="ee89f-131">Microsoft. Azure. commands. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="ee89f-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="ee89f-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ee89f-132">OUTPUTS</span></span>

### <span data-ttu-id="ee89f-133">Microsoft. Azure. commands. MixedReality. RemoteRenderingAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ee89f-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="ee89f-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ee89f-134">NOTES</span></span>

## <span data-ttu-id="ee89f-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ee89f-135">RELATED LINKS</span></span>