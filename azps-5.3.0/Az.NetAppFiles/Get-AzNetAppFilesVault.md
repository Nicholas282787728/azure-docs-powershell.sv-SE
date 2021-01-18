---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
ms.openlocfilehash: 9779db097028710aa8aeddc7a5a1c5bdea85a30a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521015"
---
# <span data-ttu-id="68569-101">Get-AzNetAppFilesVault</span><span class="sxs-lookup"><span data-stu-id="68569-101">Get-AzNetAppFilesVault</span></span>

## <span data-ttu-id="68569-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="68569-102">SYNOPSIS</span></span>
<span data-ttu-id="68569-103">Hämtar listan med NetApp-konton (ANF).</span><span class="sxs-lookup"><span data-stu-id="68569-103">Gets list of Azure NetApp Files (ANF) Accounts backup vaults.</span></span>

## <span data-ttu-id="68569-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="68569-104">SYNTAX</span></span>

### <span data-ttu-id="68569-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="68569-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVault -ResourceGroupName <String> [-AccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68569-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68569-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVault -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="68569-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68569-107">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVault -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68569-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="68569-108">DESCRIPTION</span></span>
<span data-ttu-id="68569-109">Cmdleten **Get-AzNetAppFilesVault** har en lista med säkerhets kopierings valv för ANF-konton.</span><span class="sxs-lookup"><span data-stu-id="68569-109">The **Get-AzNetAppFilesVault** cmdlet gets list of an ANF accounts backup vaults.</span></span>

## <span data-ttu-id="68569-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="68569-110">EXAMPLES</span></span>

### <span data-ttu-id="68569-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="68569-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesVault -ResourceGroupName "MyRG" -AccountName "MyAnfAccount"
```

<span data-ttu-id="68569-112">Det här kommandot får en lista med säkerhets kopierings valv för Azure NetappFiles (ANF)-konto "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="68569-112">This command gets a list of the backup vaults for Azure NetappFiles (ANF) account "MyAnfAccount".</span></span>

## <span data-ttu-id="68569-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="68569-113">PARAMETERS</span></span>

### <span data-ttu-id="68569-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="68569-114">-AccountName</span></span>
<span data-ttu-id="68569-115">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="68569-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68569-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="68569-116">-AccountObject</span></span>
<span data-ttu-id="68569-117">Kontot för det nya säkerhetskopierade objektet</span><span class="sxs-lookup"><span data-stu-id="68569-117">The account for the new backup object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68569-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68569-118">-DefaultProfile</span></span>
<span data-ttu-id="68569-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="68569-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68569-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68569-120">-ResourceGroupName</span></span>
<span data-ttu-id="68569-121">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="68569-121">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="68569-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68569-122">-ResourceId</span></span>
<span data-ttu-id="68569-123">Resurs-ID för ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="68569-123">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="68569-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68569-124">CommonParameters</span></span>
<span data-ttu-id="68569-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68569-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68569-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68569-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68569-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="68569-127">INPUTS</span></span>

### <span data-ttu-id="68569-128">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="68569-128">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="68569-129">System. String</span><span class="sxs-lookup"><span data-stu-id="68569-129">System.String</span></span>

## <span data-ttu-id="68569-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="68569-130">OUTPUTS</span></span>

### <span data-ttu-id="68569-131">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="68569-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="68569-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="68569-132">NOTES</span></span>

## <span data-ttu-id="68569-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="68569-133">RELATED LINKS</span></span>
