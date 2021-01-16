---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
ms.openlocfilehash: 677382133dffc7e64c86d02e984f35b8572a4598
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410856"
---
# <span data-ttu-id="68cef-101">Get-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="68cef-101">Get-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="68cef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="68cef-102">SYNOPSIS</span></span>
<span data-ttu-id="68cef-103">Hämtar information om ett Azure NetApp-ANF-konto.</span><span class="sxs-lookup"><span data-stu-id="68cef-103">Gets details of an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="68cef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="68cef-104">SYNTAX</span></span>

### <span data-ttu-id="68cef-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="68cef-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesAccount -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68cef-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68cef-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68cef-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="68cef-107">DESCRIPTION</span></span>
<span data-ttu-id="68cef-108">Cmdleten **Get-AzNetAppFilesAccount** hämtar information om ett ANF-konto.</span><span class="sxs-lookup"><span data-stu-id="68cef-108">The **Get-AzNetAppFilesAccount** cmdlet gets details of an ANF account.</span></span>

## <span data-ttu-id="68cef-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="68cef-109">EXAMPLES</span></span>

### <span data-ttu-id="68cef-110">Exempel 1: skaffa ett ANF-konto</span><span class="sxs-lookup"><span data-stu-id="68cef-110">Example 1: Get an ANF account</span></span>
```
PS C:\>Get-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="68cef-111">Det här kommandot får kontot MyAnfAccount.</span><span class="sxs-lookup"><span data-stu-id="68cef-111">This command gets the account named MyAnfAccount.</span></span>

## <span data-ttu-id="68cef-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="68cef-112">PARAMETERS</span></span>

### <span data-ttu-id="68cef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68cef-113">-DefaultProfile</span></span>
<span data-ttu-id="68cef-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="68cef-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68cef-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="68cef-115">-Name</span></span>
<span data-ttu-id="68cef-116">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="68cef-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68cef-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68cef-117">-ResourceGroupName</span></span>
<span data-ttu-id="68cef-118">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="68cef-118">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68cef-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68cef-119">-ResourceId</span></span>
<span data-ttu-id="68cef-120">Resurs-ID för ANF konto</span><span class="sxs-lookup"><span data-stu-id="68cef-120">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="68cef-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68cef-121">CommonParameters</span></span>
<span data-ttu-id="68cef-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68cef-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68cef-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68cef-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68cef-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="68cef-124">INPUTS</span></span>

### <span data-ttu-id="68cef-125">System. String</span><span class="sxs-lookup"><span data-stu-id="68cef-125">System.String</span></span>

## <span data-ttu-id="68cef-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="68cef-126">OUTPUTS</span></span>

### <span data-ttu-id="68cef-127">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="68cef-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="68cef-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="68cef-128">NOTES</span></span>

## <span data-ttu-id="68cef-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="68cef-129">RELATED LINKS</span></span>
