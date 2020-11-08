---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 361517912166c9548ecc69358c6dd0e776cfcd3a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261630"
---
# <span data-ttu-id="316f0-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="316f0-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="316f0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="316f0-102">SYNOPSIS</span></span>
<span data-ttu-id="316f0-103">Tar bort en Azure AD-administratör för SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="316f0-103">Removes an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="316f0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="316f0-104">SYNTAX</span></span>

### <span data-ttu-id="316f0-105">UseResourceGroupAndInstanceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="316f0-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="316f0-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="316f0-106">UseInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru]
 -InputObject <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="316f0-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="316f0-107">UserResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="316f0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="316f0-108">DESCRIPTION</span></span>
<span data-ttu-id="316f0-109">Cmdleten **Remove-AzSqlInstanceActiveDirectoryAdministrator** tar bort en Azure Active Directory-administratör (Azure AD) för AzureSQL-hanterad instans i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="316f0-109">The **Remove-AzSqlInstanceActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="316f0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="316f0-110">EXAMPLES</span></span>

### <span data-ttu-id="316f0-111">Exempel 1: ta bort en administratör</span><span class="sxs-lookup"><span data-stu-id="316f0-111">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstanceName01" -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="316f0-112">Det här kommandot tar bort Azure AD-administratören för den hanterade instans som heter ManagedInstanceName01 associerad med ResourceGroup01 för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="316f0-112">This command removes the Azure AD administrator for the managed instance named ManagedInstanceName01 associated with the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="316f0-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="316f0-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="316f0-114">Det här kommandot tar bort Azure AD-administratören från det hanterade instans-objektet.</span><span class="sxs-lookup"><span data-stu-id="316f0-114">This command removes the Azure AD administrator from the managed instance object.</span></span>

### <span data-ttu-id="316f0-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="316f0-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="316f0-116">Det här kommandot tar bort Azure AD-administratören med resurs-ID för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="316f0-116">This command removes the Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="316f0-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="316f0-117">PARAMETERS</span></span>

### <span data-ttu-id="316f0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="316f0-118">-DefaultProfile</span></span>
<span data-ttu-id="316f0-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="316f0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="316f0-120">-Force</span><span class="sxs-lookup"><span data-stu-id="316f0-120">-Force</span></span>
<span data-ttu-id="316f0-121">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="316f0-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="316f0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="316f0-122">-InputObject</span></span>
<span data-ttu-id="316f0-123">Det hanterade instans objekt som ska användas.</span><span class="sxs-lookup"><span data-stu-id="316f0-123">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="316f0-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="316f0-124">-InstanceName</span></span>
<span data-ttu-id="316f0-125">SQL-hanterat instans namn.</span><span class="sxs-lookup"><span data-stu-id="316f0-125">SQL Managed Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="316f0-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="316f0-126">-PassThru</span></span>
<span data-ttu-id="316f0-127">Definierar om den borttagna AD-administratören ska returneras</span><span class="sxs-lookup"><span data-stu-id="316f0-127">Defines whether to return the removed AD administrator</span></span>

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

### <span data-ttu-id="316f0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="316f0-128">-ResourceGroupName</span></span>
<span data-ttu-id="316f0-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="316f0-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="316f0-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="316f0-130">-ResourceId</span></span>
<span data-ttu-id="316f0-131">ID för den instans som ska användas</span><span class="sxs-lookup"><span data-stu-id="316f0-131">The resource id of instance to use</span></span>

```yaml
Type: System.String
Parameter Sets: UserResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="316f0-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="316f0-132">-Confirm</span></span>
<span data-ttu-id="316f0-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="316f0-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="316f0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="316f0-134">-WhatIf</span></span>
<span data-ttu-id="316f0-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="316f0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="316f0-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="316f0-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="316f0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="316f0-137">CommonParameters</span></span>
<span data-ttu-id="316f0-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="316f0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="316f0-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="316f0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="316f0-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="316f0-140">INPUTS</span></span>

### <span data-ttu-id="316f0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="316f0-141">System.String</span></span>

## <span data-ttu-id="316f0-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="316f0-142">OUTPUTS</span></span>

### <span data-ttu-id="316f0-143">Microsoft. Azure. commands. SQL. InstanceActiveDirectoryAdministrator. Model. AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="316f0-143">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="316f0-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="316f0-144">NOTES</span></span>

## <span data-ttu-id="316f0-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="316f0-145">RELATED LINKS</span></span>

[<span data-ttu-id="316f0-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="316f0-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="316f0-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="316f0-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)
