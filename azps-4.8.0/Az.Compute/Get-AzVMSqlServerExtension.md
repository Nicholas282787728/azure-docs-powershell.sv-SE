---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
ms.openlocfilehash: 7903e13abf7e924898910ad007eefcf6800dcc61
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258922"
---
# <span data-ttu-id="b8430-101">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b8430-101">Get-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="b8430-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8430-102">SYNOPSIS</span></span>
<span data-ttu-id="b8430-103">Hämtar inställningarna för ett SQL Server-tillägg på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="b8430-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="b8430-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8430-104">SYNTAX</span></span>

```
Get-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8430-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8430-105">DESCRIPTION</span></span>
<span data-ttu-id="b8430-106">Cmdleten **Get-AzVMSqlServerExtension** hämtar inställningarna för SQL Server-infrastrukturen som en tjänst (IaaS) Agent på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="b8430-106">The **Get-AzVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="b8430-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8430-107">EXAMPLES</span></span>

### <span data-ttu-id="b8430-108">Exempel 1: Hämta inställningar för ett SQL Server-tillägg på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="b8430-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="b8430-109">Det här kommandot får inställningar för SQL Server-tillägget på en virtuell dator med namnet ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="b8430-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="b8430-110">Exempel 2: få inställningarna genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="b8430-110">Example 2: Get the settings by using the pipeline</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service08" -Name "ContosoVM22" | Get-AzVMSqlServerExtension
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="b8430-111">Det här kommandot får den virtuella datorn som heter ContosoVM22 på tjänsten Service08 med hjälp av Get-AzVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8430-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="b8430-112">Kommandot skickar resultaten till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="b8430-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b8430-113">Det aktuella kommandot får inställningen för SQL Server IaaS-agenten på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="b8430-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="b8430-114">Exempel 3: Hämta inställningar för viss SQL Server-version</span><span class="sxs-lookup"><span data-stu-id="b8430-114">Example 3: Get the settings of specific SQL Server version</span></span>
```
PS C:\> Get-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07" -Version "1.0"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="b8430-115">Det här kommandot får inställningar för version 1,0 av SQL Server-tillägget på en virtuell dator med namnet ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="b8430-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="b8430-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8430-116">PARAMETERS</span></span>

### <span data-ttu-id="b8430-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8430-117">-DefaultProfile</span></span>
<span data-ttu-id="b8430-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b8430-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8430-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="b8430-119">-Name</span></span>
<span data-ttu-id="b8430-120">Anger namnet på SQL Server-tillägget.</span><span class="sxs-lookup"><span data-stu-id="b8430-120">Specifies the name of the SQL Server the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8430-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8430-121">-ResourceGroupName</span></span>
<span data-ttu-id="b8430-122">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="b8430-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b8430-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="b8430-123">-VMName</span></span>
<span data-ttu-id="b8430-124">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="b8430-124">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8430-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8430-125">CommonParameters</span></span>
<span data-ttu-id="b8430-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8430-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8430-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8430-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8430-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8430-128">INPUTS</span></span>

### <span data-ttu-id="b8430-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b8430-129">System.String</span></span>

## <span data-ttu-id="b8430-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8430-130">OUTPUTS</span></span>

### <span data-ttu-id="b8430-131">Microsoft. Azure. commands. Compute. VirtualMachineSqlServerExtensionContext</span><span class="sxs-lookup"><span data-stu-id="b8430-131">Microsoft.Azure.Commands.Compute.VirtualMachineSqlServerExtensionContext</span></span>

## <span data-ttu-id="b8430-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8430-132">NOTES</span></span>

## <span data-ttu-id="b8430-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8430-133">RELATED LINKS</span></span>

[<span data-ttu-id="b8430-134">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="b8430-134">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="b8430-135">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b8430-135">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="b8430-136">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b8430-136">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)

