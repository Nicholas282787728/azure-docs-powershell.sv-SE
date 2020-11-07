---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmsqlserverextension
schema: 2.0.0
ms.openlocfilehash: 6b02a83c7664fa460cd4ebd25a1754a8bc57e784
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931525"
---
# <span data-ttu-id="2e6e1-101">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="2e6e1-101">Get-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="2e6e1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2e6e1-102">SYNOPSIS</span></span>
<span data-ttu-id="2e6e1-103">Hämtar inställningarna för ett SQL Server-tillägg på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="2e6e1-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e6e1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2e6e1-104">SYNTAX</span></span>

```
Get-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e6e1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2e6e1-105">DESCRIPTION</span></span>
<span data-ttu-id="2e6e1-106">Cmdleten **Get-AzureRmVMSqlServerExtension** hämtar inställningarna för SQL Server-infrastrukturen som en tjänst (IaaS) Agent på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="2e6e1-106">The **Get-AzureRmVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="2e6e1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2e6e1-107">EXAMPLES</span></span>

### <span data-ttu-id="2e6e1-108">Exempel 1: Hämta inställningar för ett SQL Server-tillägg på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="2e6e1-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="2e6e1-109">Det här kommandot får inställningar för SQL Server-tillägget på en virtuell dator med namnet ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="2e6e1-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="2e6e1-110">Exempel 2: få inställningarna genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="2e6e1-110">Example 2: Get the settings by using the pipeline</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service08" -Name "ContosoVM22" | Get-AzureRmVMSqlServerExtension
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="2e6e1-111">Det här kommandot får den virtuella datorn som heter ContosoVM22 på tjänsten Service08 med hjälp av Get-AzureRmVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e6e1-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="2e6e1-112">Kommandot skickar resultaten till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="2e6e1-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="2e6e1-113">Det aktuella kommandot får inställningen för SQL Server IaaS-agenten på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="2e6e1-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="2e6e1-114">Exempel 3: Hämta inställningar för viss SQL Server-version</span><span class="sxs-lookup"><span data-stu-id="2e6e1-114">Example 3: Get the settings of specific SQL Server version</span></span>
```
PS C:\> Get-AzureRmVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07" -Version "1.0"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="2e6e1-115">Det här kommandot får inställningar för version 1,0 av SQL Server-tillägget på en virtuell dator med namnet ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="2e6e1-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="2e6e1-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2e6e1-116">PARAMETERS</span></span>

### <span data-ttu-id="2e6e1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e6e1-117">-DefaultProfile</span></span>
<span data-ttu-id="2e6e1-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2e6e1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e6e1-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="2e6e1-119">-Name</span></span>
<span data-ttu-id="2e6e1-120">Anger namnet på SQL Server-tillägget.</span><span class="sxs-lookup"><span data-stu-id="2e6e1-120">Specifies the name of the SQL Server the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6e1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e6e1-121">-ResourceGroupName</span></span>
<span data-ttu-id="2e6e1-122">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="2e6e1-122">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6e1-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="2e6e1-123">-VMName</span></span>
<span data-ttu-id="2e6e1-124">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="2e6e1-124">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6e1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e6e1-125">CommonParameters</span></span>
<span data-ttu-id="2e6e1-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e6e1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e6e1-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e6e1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e6e1-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2e6e1-128">INPUTS</span></span>

### <span data-ttu-id="2e6e1-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="2e6e1-129">None</span></span>
<span data-ttu-id="2e6e1-130">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="2e6e1-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2e6e1-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2e6e1-131">OUTPUTS</span></span>

### <span data-ttu-id="2e6e1-132">Microsoft. Azure. commands. Compute. VirtualMachineSqlServerExtensionContext</span><span class="sxs-lookup"><span data-stu-id="2e6e1-132">Microsoft.Azure.Commands.Compute.VirtualMachineSqlServerExtensionContext</span></span>

## <span data-ttu-id="2e6e1-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2e6e1-133">NOTES</span></span>

## <span data-ttu-id="2e6e1-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2e6e1-134">RELATED LINKS</span></span>

[<span data-ttu-id="2e6e1-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2e6e1-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="2e6e1-136">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="2e6e1-136">Remove-AzureRmVMSqlServerExtension</span></span>](./Remove-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="2e6e1-137">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="2e6e1-137">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


