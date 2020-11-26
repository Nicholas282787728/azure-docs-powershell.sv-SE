---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/set-azsqlvmconfiggroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
ms.openlocfilehash: b83dc58161791009a3adfd7cbf9b0b07b3f0b5b1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263367"
---
# <span data-ttu-id="7f183-101">Set-AzSqlVMConfigGroup</span><span class="sxs-lookup"><span data-stu-id="7f183-101">Set-AzSqlVMConfigGroup</span></span>

## <span data-ttu-id="7f183-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7f183-102">SYNOPSIS</span></span>
<span data-ttu-id="7f183-103">Ange informationen i relation till en virtuell SQL-dator grupp i en konfiguration för SQL-dator.</span><span class="sxs-lookup"><span data-stu-id="7f183-103">Set the information relative to a sql virtual machine group in a sql virtual machine configuration.</span></span>

## <span data-ttu-id="7f183-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7f183-104">SYNTAX</span></span>

```
Set-AzSqlVMConfigGroup [-SqlVM] <AzureSqlVMModel> [-SqlVMGroup] <AzureSqlVMGroupModel>
 -ClusterOperatorAccountPassword <SecureString> -SqlServiceAccountPassword <SecureString>
 [-ClusterBootstrapAccountPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f183-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7f183-105">DESCRIPTION</span></span>
<span data-ttu-id="7f183-106">Den Set-AzSqlVMConfigGroup cmdleten anger den information som behövs för att ansluta till en virtuell SQL-dator grupp för en konfiguration för SQL-dator.</span><span class="sxs-lookup"><span data-stu-id="7f183-106">The Set-AzSqlVMConfigGroup cmdlet set the information needed in order to join a sql virtual machine group for a sql virtual machine configuration.</span></span>

## <span data-ttu-id="7f183-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7f183-107">EXAMPLES</span></span>

### <span data-ttu-id="7f183-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7f183-108">Example 1</span></span>
```powershell
PS C:\> $config = Set-AzSqlVMConfigGroup -SqlVM $config -SqlVMGroup $group -ClusterOperatorAccountPassword 'password' -SqlServiceAccountPassword 'password'
```

<span data-ttu-id="7f183-109">Uppdatera grupp informationen för en konfiguration av en virtuell SQL-dator.</span><span class="sxs-lookup"><span data-stu-id="7f183-109">Update the group informations of a sql virtual machine configuration.</span></span>

## <span data-ttu-id="7f183-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7f183-110">PARAMETERS</span></span>

### <span data-ttu-id="7f183-111">-ClusterBootstrapAccountPassword</span><span class="sxs-lookup"><span data-stu-id="7f183-111">-ClusterBootstrapAccountPassword</span></span>
<span data-ttu-id="7f183-112">Lösen ord för klustrets start konto</span><span class="sxs-lookup"><span data-stu-id="7f183-112">Password for the cluster bootstrap account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f183-113">-ClusterOperatorAccountPassword</span><span class="sxs-lookup"><span data-stu-id="7f183-113">-ClusterOperatorAccountPassword</span></span>
<span data-ttu-id="7f183-114">Lösen ord för kluster operatörs kontot</span><span class="sxs-lookup"><span data-stu-id="7f183-114">Password for the cluster operator account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f183-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f183-115">-DefaultProfile</span></span>
<span data-ttu-id="7f183-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7f183-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f183-117">-SqlServiceAccountPassword</span><span class="sxs-lookup"><span data-stu-id="7f183-117">-SqlServiceAccountPassword</span></span>
<span data-ttu-id="7f183-118">Lösen ord för SQL-tjänstkontot</span><span class="sxs-lookup"><span data-stu-id="7f183-118">Password for the SQL service account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f183-119">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="7f183-119">-SqlVM</span></span>
<span data-ttu-id="7f183-120">Den konfiguration för SQL-virtuell dator vars grupp medlemskap läggs till</span><span class="sxs-lookup"><span data-stu-id="7f183-120">The SQL virtual machine configuration which group membership will be added to</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f183-121">-SqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="7f183-121">-SqlVMGroup</span></span>
<span data-ttu-id="7f183-122">Gruppen som den virtuella SQL-datorn kommer att ingå i</span><span class="sxs-lookup"><span data-stu-id="7f183-122">The group the SQL virtual machine will be part of</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f183-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f183-123">CommonParameters</span></span>
<span data-ttu-id="7f183-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f183-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f183-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f183-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f183-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7f183-126">INPUTS</span></span>

### <span data-ttu-id="7f183-127">Microsoft. Azure. commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="7f183-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="7f183-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7f183-128">OUTPUTS</span></span>

### <span data-ttu-id="7f183-129">Microsoft. Azure. commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="7f183-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="7f183-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7f183-130">NOTES</span></span>

## <span data-ttu-id="7f183-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7f183-131">RELATED LINKS</span></span>