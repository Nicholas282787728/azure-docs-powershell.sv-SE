---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
ms.openlocfilehash: fc4a0624b6e5702c0ef0c836f0b6ac593c25dafe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523943"
---
# <span data-ttu-id="ef754-101">Get-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="ef754-101">Get-AzSqlVMGroup</span></span>

## <span data-ttu-id="ef754-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef754-102">SYNOPSIS</span></span>
<span data-ttu-id="ef754-103">Hämtar en eller flera virtuella SQL-datorer.</span><span class="sxs-lookup"><span data-stu-id="ef754-103">Gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="ef754-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef754-104">SYNTAX</span></span>

### <span data-ttu-id="ef754-105">ResourceGroupOnly (standard)</span><span class="sxs-lookup"><span data-stu-id="ef754-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVMGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ef754-106">Namn</span><span class="sxs-lookup"><span data-stu-id="ef754-106">Name</span></span>
```
Get-AzSqlVMGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ef754-107">ID</span><span class="sxs-lookup"><span data-stu-id="ef754-107">ResourceId</span></span>
```
Get-AzSqlVMGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef754-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef754-108">DESCRIPTION</span></span>
<span data-ttu-id="ef754-109">Med den Get-AzSqlVMGroup cmdleten hämtas en eller flera virtuella SQL-datorer.</span><span class="sxs-lookup"><span data-stu-id="ef754-109">The Get-AzSqlVMGroup cmdlet gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="ef754-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef754-110">EXAMPLES</span></span>

### <span data-ttu-id="ef754-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ef754-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup

Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
group1     ResourceGroup02    Developer SQL2017-WS2016
```

<span data-ttu-id="ef754-112">Med det här kommandot får du information om alla virtuella Azure SQL-datorer i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="ef754-112">This command gets information about all the Azure SQL virtual machine groups in the current subscription.</span></span>

### <span data-ttu-id="ef754-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ef754-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="ef754-114">Med det här kommandot får du information om alla virtuella Azure SQL-datorer i den aktuella prenumerationen som har tilldelats till resurs gruppen ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="ef754-114">This command gets information about all the Azure SQL virtual machine groups in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="ef754-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="ef754-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="ef754-116">Det här kommandot får information om den virtuella SQL-dator gruppen "test-grupp" som tilldelats ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="ef754-116">This command gets information about the SQL virtual machine group "test-group" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="ef754-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef754-117">PARAMETERS</span></span>

### <span data-ttu-id="ef754-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef754-118">-DefaultProfile</span></span>
<span data-ttu-id="ef754-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ef754-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef754-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="ef754-120">-Name</span></span>
<span data-ttu-id="ef754-121">Namn på en virtuell dator i SQL.</span><span class="sxs-lookup"><span data-stu-id="ef754-121">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef754-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef754-122">-ResourceGroupName</span></span>
<span data-ttu-id="ef754-123">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ef754-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="ef754-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef754-124">-ResourceId</span></span>
<span data-ttu-id="ef754-125">Grupp-ID för virtuell dator i SQL.</span><span class="sxs-lookup"><span data-stu-id="ef754-125">SQL virtual machine group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef754-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef754-126">CommonParameters</span></span>
<span data-ttu-id="ef754-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef754-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef754-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef754-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef754-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef754-129">INPUTS</span></span>

### <span data-ttu-id="ef754-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ef754-130">System.String</span></span>

## <span data-ttu-id="ef754-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef754-131">OUTPUTS</span></span>

### <span data-ttu-id="ef754-132">Microsoft. Azure. commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="ef754-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="ef754-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef754-133">NOTES</span></span>

## <span data-ttu-id="ef754-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef754-134">RELATED LINKS</span></span>
