---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccount.md
ms.openlocfilehash: 9d4faa4a51352902330286722a005fae1b42bef7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416899"
---
# <span data-ttu-id="b2b9e-101">Get-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="b2b9e-101">Get-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="b2b9e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b2b9e-102">SYNOPSIS</span></span>
<span data-ttu-id="b2b9e-103">Skaffa fjärrstyrt konto</span><span class="sxs-lookup"><span data-stu-id="b2b9e-103">Get Remote Rendering Account</span></span>

## <span data-ttu-id="b2b9e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b2b9e-104">SYNTAX</span></span>

### <span data-ttu-id="b2b9e-105">ListParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b2b9e-105">ListParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccount [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2b9e-106">GetParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b2b9e-106">GetParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2b9e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2b9e-107">ResourceIdParameterSet</span></span>
```
Get-AzRemoteRenderingAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2b9e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b2b9e-108">DESCRIPTION</span></span>
<span data-ttu-id="b2b9e-109">Hämta eller Visa fjärråter givnings konton i vissa abonnemang och resurs grupper.</span><span class="sxs-lookup"><span data-stu-id="b2b9e-109">Get or list Remote Rendering Account(s) in certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="b2b9e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b2b9e-110">EXAMPLES</span></span>

### <span data-ttu-id="b2b9e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b2b9e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/RemoteRenderingAccounts/example
Name                : example
Type                : Microsoft.MixedReality/RemoteRenderingAccounts

ResourceGroupName   : rg1
AccountId           : 2f7443d0-2c2b-4514-9b29-a78072a1556f
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/2f7443d0-2c2b-4514-9b29-a78072a1556f/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/RemoteRenderingAccounts/demo
Name                : demo
Type                : Microsoft.MixedReality/RemoteRenderingAccounts

ResourceGroupName   : rg1
AccountId           : ed3273ce-1eeb-42c7-b3b8-fb9896b9801c
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/ed3273ce-1eeb-42c7-b3b8-fb9896b9801c/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/RemoteRenderingAccounts/foobar
Name                : foobar
Type                : Microsoft.MixedReality/RemoteRenderingAccounts
```

<span data-ttu-id="b2b9e-112">Lista alla fjär åter givnings konton i resurs gruppen "RG1".</span><span class="sxs-lookup"><span data-stu-id="b2b9e-112">List all Remote Rendering Account in Resource Group "rg1".</span></span> 

### <span data-ttu-id="b2b9e-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b2b9e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mrc-anchor-prod.trafficmanager.net
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/RemoteRenderingAccounts/example
Name                : example
Type                : Microsoft.MixedReality/RemoteRenderingAccounts
```

<span data-ttu-id="b2b9e-114">Skaffa Remote rendering-konto "exempel" i resurs gruppen "RG1".</span><span class="sxs-lookup"><span data-stu-id="b2b9e-114">Get Remote Rendering Account "example" in Resource Group "rg1".</span></span> 

## <span data-ttu-id="b2b9e-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b2b9e-115">PARAMETERS</span></span>

### <span data-ttu-id="b2b9e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2b9e-116">-DefaultProfile</span></span>
<span data-ttu-id="b2b9e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b2b9e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2b9e-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="b2b9e-118">-Name</span></span>
<span data-ttu-id="b2b9e-119">Namn på fjärrrendering-konto.</span><span class="sxs-lookup"><span data-stu-id="b2b9e-119">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: GetParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2b9e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2b9e-120">-ResourceGroupName</span></span>
<span data-ttu-id="b2b9e-121">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="b2b9e-121">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListParameterSet
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2b9e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2b9e-122">-ResourceId</span></span>
<span data-ttu-id="b2b9e-123">Resurs-ID för fjärrstyrt konto.</span><span class="sxs-lookup"><span data-stu-id="b2b9e-123">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="b2b9e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2b9e-124">CommonParameters</span></span>
<span data-ttu-id="b2b9e-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2b9e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b2b9e-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2b9e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2b9e-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b2b9e-127">INPUTS</span></span>

### <span data-ttu-id="b2b9e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b2b9e-128">System.String</span></span>

## <span data-ttu-id="b2b9e-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b2b9e-129">OUTPUTS</span></span>

### <span data-ttu-id="b2b9e-130">Microsoft. Azure. commands. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="b2b9e-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="b2b9e-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b2b9e-131">NOTES</span></span>

## <span data-ttu-id="b2b9e-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b2b9e-132">RELATED LINKS</span></span>
