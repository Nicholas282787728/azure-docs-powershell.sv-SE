---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8CE8F4E9-93D4-41E5-8B43-F886C018D9FB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06681544df4974a1ee906552af96302698e88d74
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093256"
---
# <span data-ttu-id="25d94-101">Get-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="25d94-101">Get-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="25d94-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="25d94-102">SYNOPSIS</span></span>
<span data-ttu-id="25d94-103">Hämtar inställningarna för SQL Server IaaS agent på en viss virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="25d94-103">Gets the settings of the SQL Server IaaS Agent on a particular virtual machine.</span></span>

## <span data-ttu-id="25d94-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="25d94-104">SYNTAX</span></span>

```
Get-AzureVMSqlServerExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="25d94-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="25d94-105">DESCRIPTION</span></span>
<span data-ttu-id="25d94-106">Cmdleten **Get-AzureVMSqlServerExtension** hämtar inställningar för SQL Server-infrastrukturen som tjänst (IaaS) Agent på en viss virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="25d94-106">The **Get-AzureVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a particular virtual machine.</span></span>

## <span data-ttu-id="25d94-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="25d94-107">EXAMPLES</span></span>

### <span data-ttu-id="25d94-108">Exempel 1: Hämta inställningar för ett SQL Server-tillägg på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="25d94-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureVMSqlServerExtension-VM $VM
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="25d94-109">Hämtar inställningar för SQL Server-tillägget på en viss virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="25d94-109">Gets the settings of the SQL Server extension on a particular virtual machine.</span></span>

### <span data-ttu-id="25d94-110">Exempel 2: Hämta inställningar för SQL Server IaaS agent på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="25d94-110">Example 2: Get the settings of a SQL Server IaaS Agent on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Get-AzureVMSqlServerExtension
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="25d94-111">Hämtar inställningarna för SQL Server IaaS agent på en viss virtuell dator med piped-inmatning.</span><span class="sxs-lookup"><span data-stu-id="25d94-111">Gets the settings of the SQL Server IaaS Agent on a particular virtual machine using piped input.</span></span>

### <span data-ttu-id="25d94-112">Exempel 3: Hämta inställningar för viss SQL Server-version IaaS agent på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="25d94-112">Example 3: Get the settings of specific SQL Server version IaaS Agent on a virtual machine</span></span>
```
PS C:\> Get-AzureVMSqlServerExtension -VM $VM -Version "1.0"
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="25d94-113">Det här kommandot får inställningarna för den specifika versionen av SQL Server IaaS agent på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="25d94-113">This command gets the settings of the particular version of SQL Server IaaS Agent on a virtual machine.</span></span>

## <span data-ttu-id="25d94-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="25d94-114">PARAMETERS</span></span>

### <span data-ttu-id="25d94-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="25d94-115">-InformationAction</span></span>
<span data-ttu-id="25d94-116">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="25d94-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="25d94-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="25d94-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="25d94-118">Vidare</span><span class="sxs-lookup"><span data-stu-id="25d94-118">Continue</span></span>
- <span data-ttu-id="25d94-119">Över</span><span class="sxs-lookup"><span data-stu-id="25d94-119">Ignore</span></span>
- <span data-ttu-id="25d94-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="25d94-120">Inquire</span></span>
- <span data-ttu-id="25d94-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="25d94-121">SilentlyContinue</span></span>
- <span data-ttu-id="25d94-122">Stanna</span><span class="sxs-lookup"><span data-stu-id="25d94-122">Stop</span></span>
- <span data-ttu-id="25d94-123">Avbryt</span><span class="sxs-lookup"><span data-stu-id="25d94-123">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25d94-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="25d94-124">-InformationVariable</span></span>
<span data-ttu-id="25d94-125">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="25d94-125">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25d94-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="25d94-126">-Profile</span></span>
<span data-ttu-id="25d94-127">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="25d94-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="25d94-128">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="25d94-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25d94-129">-VM</span><span class="sxs-lookup"><span data-stu-id="25d94-129">-VM</span></span>
<span data-ttu-id="25d94-130">Anger det beständiga virtuella dator objekt som denna cmdlet hämtar inställningar från.</span><span class="sxs-lookup"><span data-stu-id="25d94-130">Specifies the persistent virtual machine object that this cmdlet gets settings from.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25d94-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25d94-131">CommonParameters</span></span>
<span data-ttu-id="25d94-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25d94-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25d94-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25d94-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25d94-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="25d94-134">INPUTS</span></span>

## <span data-ttu-id="25d94-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="25d94-135">OUTPUTS</span></span>

## <span data-ttu-id="25d94-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="25d94-136">NOTES</span></span>

## <span data-ttu-id="25d94-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="25d94-137">RELATED LINKS</span></span>

[<span data-ttu-id="25d94-138">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="25d94-138">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)

[<span data-ttu-id="25d94-139">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="25d94-139">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)


