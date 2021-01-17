---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
ms.openlocfilehash: b6f5b885e2cb65c8cf4775f8bb37742b8d98b6a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413451"
---
# <span data-ttu-id="cb38a-101">Get-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="cb38a-101">Get-AzSqlVM</span></span>

## <span data-ttu-id="cb38a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cb38a-102">SYNOPSIS</span></span>
<span data-ttu-id="cb38a-103">Hämtar en eller flera virtuella SQL-datorer.</span><span class="sxs-lookup"><span data-stu-id="cb38a-103">Gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="cb38a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cb38a-104">SYNTAX</span></span>

### <span data-ttu-id="cb38a-105">ResourceGroupOnly (standard)</span><span class="sxs-lookup"><span data-stu-id="cb38a-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVM [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb38a-106">Namn</span><span class="sxs-lookup"><span data-stu-id="cb38a-106">Name</span></span>
```
Get-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cb38a-107">ID</span><span class="sxs-lookup"><span data-stu-id="cb38a-107">ResourceId</span></span>
```
Get-AzSqlVM [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb38a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cb38a-108">DESCRIPTION</span></span>
<span data-ttu-id="cb38a-109">Med den Get-AzSqlVM cmdleten hämtas en eller flera virtuella SQL-datorer.</span><span class="sxs-lookup"><span data-stu-id="cb38a-109">The Get-AzSqlVM cmdlet gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="cb38a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cb38a-110">EXAMPLES</span></span>

### <span data-ttu-id="cb38a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cb38a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVM

Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
vm2  ResourceGroup02    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="cb38a-112">Det här kommandot får information om alla virtuella Azure SQL-datorer i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="cb38a-112">This command gets information about all the Azure SQL virtual machines in the current subscription.</span></span>

### <span data-ttu-id="cb38a-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="cb38a-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="cb38a-114">Med det här kommandot får du information om alla virtuella Azure SQL-datorer i den aktuella prenumerationen som har tilldelats till resurs gruppen ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="cb38a-114">This command gets information about all the Azure SQL virtual machines in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="cb38a-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="cb38a-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="cb38a-116">Med det här kommandot får du information om den virtuella SQL-datorn som har tilldelats till resurs gruppen ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="cb38a-116">This command gets information about the SQL virtual machine "vm" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="cb38a-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cb38a-117">PARAMETERS</span></span>

### <span data-ttu-id="cb38a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb38a-118">-DefaultProfile</span></span>
<span data-ttu-id="cb38a-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cb38a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb38a-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="cb38a-120">-Name</span></span>
<span data-ttu-id="cb38a-121">Namn på SQL-dator.</span><span class="sxs-lookup"><span data-stu-id="cb38a-121">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb38a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb38a-122">-ResourceGroupName</span></span>
<span data-ttu-id="cb38a-123">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="cb38a-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupOnly
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb38a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb38a-124">-ResourceId</span></span>
<span data-ttu-id="cb38a-125">Resurs-ID för virtuell dator i SQL.</span><span class="sxs-lookup"><span data-stu-id="cb38a-125">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb38a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb38a-126">CommonParameters</span></span>
<span data-ttu-id="cb38a-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb38a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb38a-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb38a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb38a-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cb38a-129">INPUTS</span></span>

### <span data-ttu-id="cb38a-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="cb38a-130">None</span></span>

## <span data-ttu-id="cb38a-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cb38a-131">OUTPUTS</span></span>

### <span data-ttu-id="cb38a-132">Microsoft. Azure. commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="cb38a-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="cb38a-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cb38a-133">NOTES</span></span>

## <span data-ttu-id="cb38a-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cb38a-134">RELATED LINKS</span></span>
