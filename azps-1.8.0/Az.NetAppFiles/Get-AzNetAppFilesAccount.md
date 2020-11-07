---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
ms.openlocfilehash: dbe206a744cc0a80d166d93b09ff0ab000cb3bc6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754015"
---
# <span data-ttu-id="61005-101">Get-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="61005-101">Get-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="61005-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="61005-102">SYNOPSIS</span></span>
<span data-ttu-id="61005-103">Hämtar information om ett Azure NetApp-ANF-konto.</span><span class="sxs-lookup"><span data-stu-id="61005-103">Gets details of an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="61005-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="61005-104">SYNTAX</span></span>

### <span data-ttu-id="61005-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="61005-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesAccount -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61005-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61005-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61005-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="61005-107">DESCRIPTION</span></span>
<span data-ttu-id="61005-108">Cmdleten **Get-AzNetAppFilesAccount** hämtar information om ett ANF-konto.</span><span class="sxs-lookup"><span data-stu-id="61005-108">The **Get-AzNetAppFilesAccount** cmdlet gets details of an ANF account.</span></span>

## <span data-ttu-id="61005-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="61005-109">EXAMPLES</span></span>

### <span data-ttu-id="61005-110">Exempel 1: skaffa ett ANF-konto</span><span class="sxs-lookup"><span data-stu-id="61005-110">Example 1: Get an ANF account</span></span>
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

<span data-ttu-id="61005-111">Det här kommandot får kontot MyAnfAccount.</span><span class="sxs-lookup"><span data-stu-id="61005-111">This command gets the account named MyAnfAccount.</span></span>

## <span data-ttu-id="61005-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="61005-112">PARAMETERS</span></span>

### <span data-ttu-id="61005-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61005-113">-DefaultProfile</span></span>
<span data-ttu-id="61005-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="61005-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61005-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="61005-115">-Name</span></span>
<span data-ttu-id="61005-116">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="61005-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61005-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61005-117">-ResourceGroupName</span></span>
<span data-ttu-id="61005-118">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="61005-118">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61005-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61005-119">-ResourceId</span></span>
<span data-ttu-id="61005-120">Resurs-ID för ANF konto</span><span class="sxs-lookup"><span data-stu-id="61005-120">The resource id of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61005-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61005-121">CommonParameters</span></span>
<span data-ttu-id="61005-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61005-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="61005-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61005-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61005-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="61005-124">INPUTS</span></span>

### <span data-ttu-id="61005-125">System. String</span><span class="sxs-lookup"><span data-stu-id="61005-125">System.String</span></span>

## <span data-ttu-id="61005-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="61005-126">OUTPUTS</span></span>

### <span data-ttu-id="61005-127">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="61005-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="61005-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="61005-128">NOTES</span></span>

## <span data-ttu-id="61005-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="61005-129">RELATED LINKS</span></span>
