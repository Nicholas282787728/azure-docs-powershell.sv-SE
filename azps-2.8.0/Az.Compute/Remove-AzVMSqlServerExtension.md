---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 81acbdd914d4a3cdb69da9ac0d2093f4e1dd4cdf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745010"
---
# <span data-ttu-id="eef51-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="eef51-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="eef51-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eef51-102">SYNOPSIS</span></span>
<span data-ttu-id="eef51-103">Tar bort ett SQL Server-tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="eef51-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="eef51-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eef51-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eef51-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eef51-105">DESCRIPTION</span></span>
<span data-ttu-id="eef51-106">Cmdleten **Remove-AzVMSqlServerExtension** tar bort ett AzureSQL-tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="eef51-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="eef51-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eef51-107">EXAMPLES</span></span>

### <span data-ttu-id="eef51-108">Exempel 1: ta bort ett SQL Server-tillägg</span><span class="sxs-lookup"><span data-stu-id="eef51-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="eef51-109">Det här kommandot tar bort ett SQL Server-tillägg från den virtuella datorn med namnet ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="eef51-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="eef51-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eef51-110">PARAMETERS</span></span>

### <span data-ttu-id="eef51-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eef51-111">-DefaultProfile</span></span>
<span data-ttu-id="eef51-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eef51-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eef51-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="eef51-113">-Name</span></span>
<span data-ttu-id="eef51-114">Anger namnet på SQL Server tillägget som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="eef51-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eef51-115">-Nowait</span><span class="sxs-lookup"><span data-stu-id="eef51-115">-NoWait</span></span>
<span data-ttu-id="eef51-116">Startar operationen och returnerar omedelbart innan operationen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="eef51-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="eef51-117">Använd en annan mekanism för att avgöra om åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="eef51-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eef51-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eef51-118">-ResourceGroupName</span></span>
<span data-ttu-id="eef51-119">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="eef51-119">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eef51-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="eef51-120">-VMName</span></span>
<span data-ttu-id="eef51-121">Anger namnet på den virtuella dator från vilken denna cmdlet tar bort SQL Server-tillägget.</span><span class="sxs-lookup"><span data-stu-id="eef51-121">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eef51-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eef51-122">CommonParameters</span></span>
<span data-ttu-id="eef51-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eef51-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eef51-124">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eef51-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eef51-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eef51-125">INPUTS</span></span>

### <span data-ttu-id="eef51-126">System. String</span><span class="sxs-lookup"><span data-stu-id="eef51-126">System.String</span></span>

## <span data-ttu-id="eef51-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eef51-127">OUTPUTS</span></span>

### <span data-ttu-id="eef51-128">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="eef51-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="eef51-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eef51-129">NOTES</span></span>

## <span data-ttu-id="eef51-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eef51-130">RELATED LINKS</span></span>

[<span data-ttu-id="eef51-131">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="eef51-131">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="eef51-132">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="eef51-132">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)

