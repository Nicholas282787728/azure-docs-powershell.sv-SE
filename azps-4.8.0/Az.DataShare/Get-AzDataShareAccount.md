---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
ms.openlocfilehash: 777c3dd8214288a3f7c5b5be92a65260bf8c6c98
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102913"
---
# <span data-ttu-id="42a2a-101">Get-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="42a2a-101">Get-AzDataShareAccount</span></span>

## <span data-ttu-id="42a2a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="42a2a-102">SYNOPSIS</span></span>
<span data-ttu-id="42a2a-103">Hämtar information om DataShare-konton</span><span class="sxs-lookup"><span data-stu-id="42a2a-103">Gets information about DataShare Accounts</span></span>

## <span data-ttu-id="42a2a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="42a2a-104">SYNTAX</span></span>

### <span data-ttu-id="42a2a-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="42a2a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42a2a-106">ByResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="42a2a-106">ByResourceGroupParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="42a2a-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="42a2a-107">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42a2a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="42a2a-108">DESCRIPTION</span></span>
<span data-ttu-id="42a2a-109">Cmdleten **Get-AzDataShareAccount** hämtar information om datashare-konton i en Azure-prenumeration/resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="42a2a-109">The **Get-AzDataShareAccount** cmdlet gets information about datashare accounts in an Azure subscription / resource group.</span></span>
<span data-ttu-id="42a2a-110">Om du anger namnet på ett konto får denna cmdlet information om det datshare-kontot.</span><span class="sxs-lookup"><span data-stu-id="42a2a-110">If you specify the name of an account, this cmdlet gets information about that datshare account.</span></span>
<span data-ttu-id="42a2a-111">Om du inte anger ett namn hämtas den här cmdleten information om alla datashare-konton i en Azure-prenumeration/resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="42a2a-111">If you do not specify a name, this cmdlet gets information about all of the datashare accounts in an Azure subscription / resource group.</span></span>

## <span data-ttu-id="42a2a-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="42a2a-112">EXAMPLES</span></span>

### <span data-ttu-id="42a2a-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="42a2a-113">Example 1</span></span>
```
PS C:\> Get-AzDataShareAccount -ResourceGroupName "ADS"
DataShareAccountName    : WikiADS
ResourceGroupName       : ADS
Location                : WestUS
ProvisioningState       : Succeeded
Tags                    : {}
Identity                : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type                    : Microsoft.DataShare/accounts
Id                      : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
DataShareAccountName    : WikiADS2
ResourceGroupName       : ADS
Location                : westus
ProvisioningState       : Succeeded
Tags                    : {}
Identity                : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type                    : Microsoft.DataShare/accounts
Id                      : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
```

<span data-ttu-id="42a2a-114">Det här kommandot visar information om alla datashare-konton i Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="42a2a-114">This command displays information about all datashare accounts in the Azure subscription.</span></span>

## <span data-ttu-id="42a2a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="42a2a-115">PARAMETERS</span></span>

### <span data-ttu-id="42a2a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42a2a-116">-DefaultProfile</span></span>
<span data-ttu-id="42a2a-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="42a2a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42a2a-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="42a2a-118">-Name</span></span>
<span data-ttu-id="42a2a-119">Namn på Azure Data Share-konto.</span><span class="sxs-lookup"><span data-stu-id="42a2a-119">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42a2a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42a2a-120">-ResourceGroupName</span></span>
<span data-ttu-id="42a2a-121">Resurs grupp namnet för Azure Data Share-kontot.</span><span class="sxs-lookup"><span data-stu-id="42a2a-121">The resource group name of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42a2a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42a2a-122">-ResourceId</span></span>
<span data-ttu-id="42a2a-123">Resurs-ID för Azure Data Share-kontot.</span><span class="sxs-lookup"><span data-stu-id="42a2a-123">The resource id of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42a2a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42a2a-124">CommonParameters</span></span>
<span data-ttu-id="42a2a-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42a2a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42a2a-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42a2a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42a2a-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="42a2a-127">INPUTS</span></span>

### <span data-ttu-id="42a2a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="42a2a-128">System.String</span></span>

## <span data-ttu-id="42a2a-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="42a2a-129">OUTPUTS</span></span>

### <span data-ttu-id="42a2a-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="42a2a-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="42a2a-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="42a2a-131">NOTES</span></span>

## <span data-ttu-id="42a2a-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="42a2a-132">RELATED LINKS</span></span>
